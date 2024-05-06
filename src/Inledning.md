# Distribution av operativsystem på nätverk  

## Översikt över processen

En klient med PXE (Preboot eXecution Environment) aktiverad i sitt NIC(Network Interface Controller) har stöd för BOOTP (Bootstrap Protocol). Detta protokoll, som hanteras av en DHCP-server, gör det möjligt för klienten att få sin egen IP-adress samt information om var den kan hämta bootloadern.

Sekvensen är enligt följande:

1. Klientens PXE-aktiverade NIC sänder ut sin MAC-adress (Medium access control) och begär en IP-adress från en BOOTP/DHCP-server.

2. DHCP/BOOTP-servern, som kan vara konfigurerad med klientens MAC-adress och andra alternativ, returnerar en IP-adress till klienten tillsammans med namnet på TFTP-servern (Trivial File Transfer Protocol) och namnet på bootloader-filen, NBP (Network Boot Program), som finns på TFTP-servern.

3. Klienten använder TFTP för att hämta bootloader-filen från TFTP-servern som tillhandahåller namnet på (*.ISO) filen den skall ladda. Därefter kör klienten filen och återfår sin IP-adress från DHCP-servern.  

</br>  

````mermaid  
%%{
  init: {
    'theme': 'base',
    'themeVariables': {
      'primaryColor': '#abcadf',
      'primaryTextColor': '#3e3e3e',
      'primaryBorderColor': '#bfd2df',
      'lineColor': '#bfbfbf'
      
      
    }
  }
}%%


sequenceDiagram

    Autonumber
    Klient->> DHCP: Jag vill ha en DHCP- & PXE-server.
    DHCP->>Klient: Jag är en DHCP-server.
    DHCP-->> Klient: Skickar adressen till PXE-servern.
    iVentoy->> Klient: Jag är en PXE-server.

    Klient->> DHCP: Jag vill ha en IP-adress.
    DHCP-->> Klient: Skickar en IP-adress.
    Klient->>iVentoy: Jag vill ha sökvägen till NBP-filen.
    iVentoy-->>Klient: Skickar sökvägen till NBP-filen.
    Klient-> iVentoy: Hämtar & kör NBP-filen.
    iVentoy->> Klient: iVentoy sänder operativsystemet. 
   
   
    Note right of iVentoy: iVentoy kör TFTP-<br/>servern som sänder<br/>via UDP Port 69.



````

I DHCP-servern är det Option 66 och Option 67 som skall ställas in i "Scope options" med den information som krävs.  

* Option 66 anger vilken server som ska kontaktas

* Option 67 anger namnet på den bootloader-fil som ska begäras.  

Den här metoden fungerar bra när klienterna befinner sig i samma del av nätverket som servrarna och har enhetlig arkitektur.
Men när klienterna befinner sig i en annan del av nätverket än servrarna, eller om det finns en blandning av BIOS-, UEFI-, 32-bitars-, 64-bitars- och ARM-enheter, blir det lite rörigt. Var och en av dessa klienter behöver en specifik bootloader-fil som levereras till dem och DHCP-servern låter dig bara ange _en_ bootloader-fil. iVentoy har dock en lösning.

iVentoy kör den interna DHCP-servern parallellt med den externa men svarar inte på anrop. Däremot samlas information in om klienternas firmware; BIOS eller UEFI. Det virtuella filnamnet iventoy_loader_16000 som DHCP-servern sänder är betet, men korrekt bootloader-fil sänds till respektive firmware-version.  

Knivigare blir det när DHCP-servern befinner sig i ett annat LAN/VLAN. DHCP-servern som befinner sig på det externa nätet samlar in information om firmware-versioner och måste konfigureras så att varje klient får korrekt bootloader-fil. Detta ställer krav på DHCP-servern som måste kunna ställa in en sån konfiguration. Windows DHCP-server klarar inte det, så den här guiden täcker inte den lösningen.  
