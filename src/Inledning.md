# Distribution av programvara över nätverk

#### iVentoy – gratis programvara gör det smidigare  

</br>  

## Sammanfattning  

Uppgiften är att distribuera Windows 10 över nätverk och dokumentera arbetet. Ett smidigt alternativ för en obevakad process presenteras liksom tre alternativa värd-servrar. iVentoy kan köras från t.ex. Windows 10 Home, men är inte dokumenterad i guiden. Problem som har dykt upp har dokumenterats och lösningar har presenterats. I de fall extra programvara har krävts för att lösa problem har guider skapats.

### 1. Bakgrund

Jag var nyfiken på hur en installation över nätverk skulle gå tillväga och hur man gjorde en obevakad installation.

#### 1.1 Syfte

Syftet är att lära mig hur en massdistribuering skall gå tillväga på ett effektivt vis.

#### 1.2 Frågeställning/Mål

Jag ville lära mig hur olika operativsystem skulle konfigureras för uppgiften. En tanke var också installera en mängd programvaror under processen, men det fanns ingen lösning på det. Winget löser det enkelt med skript efter installationen, men det ligger utanför uppgiften.

#### 1.3 Metod och material

Jag har främst använt mig av gratisprogram: Hyper-V, iVentoy och mdBook. Om man inte har tillgång till Hyper-V kan man t.ex. använda Qemu.

### 2. Genomförande

#### 2.1 Arbetsprocess

Dokumentationen av iVentoy lästes igenom. Processen mellan server, DHCP och klient fick utrönas med hjälp av Google, som så mycket annat. En del av sökresultaten var utdaterade, så det blev lite strul emellanåt. Informationen var inte alltid enhetlig vilket också utgjorde ett problem. Test gjordes i skolans nätverk för att se att det funkade ”live”, sen gjordes resten i Hyper-V. Då programvara och OS uppdateras fortlöpande stötte man på en del kommandon och program som inte funkade. Man fick testa sig fram.

#### 2.2 Dokumentation

För dokumentationen användes mdBook som primärt använder Markdown syntax för textformatering. mdBook kräver att Rust, MSVC, Windows 10 eller 11 SDK, Cmake och VS Code eller likvärdig källkodsredigerare installeras. Det fanns en del dokumentation att gå igenom, även på insticksprogrammen som inte funkade korrekt eller som behövde modifieras. Html-kod behövde även läggas till Mermaid efter att ha processats i mdBook. Inforutorna i guiden tillhör ett insticksprogram som modifierades med CSS och kompilerades till .exe med Rust. Screentogif användes för video och konverterades till mp4 med ffmpeg. Faststone Capture användes för skärmbilder. Dokumentationen tog lång tid att göra men kommer till nytta framöver förhoppningsvis.

### 3. Avslutning/ Utvärdering

Det har varit kul att göra arbetet då man fått lära sig mycket nytt. Speciellt Linux var kul och nyttigt att arbeta med. iVentoy utvecklas fortlöpande viket alla programvaror gör. Under tiden jag skrivit guiden har Ubuntu hunnit släppa en ny version, likaså har autounattend-skriptet uppdaterats tre gånger. Det är nu lättare att förstå varför mycket av det jag googlat var utdaterat.

Författare: Thorbjörn Jensen  
Lärare: Peter Berger  
Movant Lund  
