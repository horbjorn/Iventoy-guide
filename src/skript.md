# Skript  

En skriptfil ger möjligheten att få en obevakad installation och kan samtidigt, i viss mån, förhindra installation av icke önskvärd programvara. Skriptinställningarna kan ställas in på t.ex. [denna sidan](https://schneegans.de/windows/unattend-generator/) och går att ladda ner samt sparas som bokmärke. Jag har använt [dessa inställningar](https://schneegans.de/windows/unattend-generator/?LanguageMode=Unattended&UILanguage=en-US&UserLocale=sv-SE&KeyboardLayout=041d%3A0000041d&GeoLocation=221&ProcessorArchitecture=amd64&ComputerNameMode=Random&TimeZoneMode=Implicit&PartitionMode=Unattended&PartitionLayout=GPT&EspSize=300&RecoveryMode=Partition&RecoverySize=1000&WindowsEditionMode=Unattended&WindowsEdition=pro&UserAccountMode=Unattended&AccountName0=Admin&AccountPassword0=password&AccountGroup0=Administrators&AccountName1=&AccountName2=&AccountName3=&AccountName4=&AutoLogonMode=Own&PasswordExpirationMode=Default&LockoutMode=Default&DisableSystemRestore=true&EnableLongPaths=true&HardenSystemDriveAcl=true&AllowPowerShellScripts=true&DisableLastAccess=true&NoAutoRebootWithLoggedOnUsers=true&TurnOffSystemSounds=true&DisableAppSuggestions=true&DisableWidgets=true&WifiMode=Interactive&ExpressSettings=DisableAll&Remove3DViewer=true&RemoveBingSearch=true&RemoveCalculator=true&RemoveCamera=true&RemoveClipchamp=true&RemoveClock=true&RemoveCopilot=true&RemoveCortana=true&RemoveDevHome=true&RemoveFamily=true&RemoveFeedbackHub=true&RemoveGetHelp=true&RemoveInternetExplorer=true&RemoveMailCalendar=true&RemoveMaps=true&RemoveMathInputPanel=true&RemoveNews=true&RemoveNotepadClassic=true&RemoveOneDrive=true&RemoveOneNote=true&RemoveOpenSSHClient=true&RemovePaint=true&RemovePaint3D=true&RemovePeople=true&RemovePhotos=true&RemovePowerAutomate=true&RemovePowerShellISE=true&RemoveQuickAssist=true&RemoveSkype=true&RemoveSnippingTool=true&RemoveSolitaire=true&RemoveStepsRecorder=true&RemoveStickyNotes=true&RemoveTeams=true&RemoveGetStarted=true&RemoveToDo=true&RemoveVoiceRecorder=true&RemoveWeather=true&RemoveWindowsMediaPlayer=true&RemoveZuneMusic=true&RemoveWindowsTerminal=true&RemoveWordPad=true&RemoveXboxApps=true&RemoveYourPhone=true&SystemScript0=&SystemScriptType0=Cmd&SystemScript1=&SystemScriptType1=Ps1&SystemScript2=&SystemScriptType2=Reg&SystemScript3=&SystemScriptType3=Vbs&DefaultUserScript0=&DefaultUserScriptType0=Reg&DefaultUserScript1=&DefaultUserScriptType1=Reg&DefaultUserScript2=&DefaultUserScriptType2=Reg&DefaultUserScript3=&DefaultUserScriptType3=Reg&FirstLogonScript0=&FirstLogonScriptType0=Cmd&FirstLogonScript1=&FirstLogonScriptType1=Ps1&FirstLogonScript2=&FirstLogonScriptType2=Reg&FirstLogonScript3=&FirstLogonScriptType3=Vbs&UserOnceScript0=&UserOnceScriptType0=Cmd&UserOnceScript1=&UserOnceScriptType1=Ps1&UserOnceScript2=&UserOnceScriptType2=Reg&UserOnceScript3=&UserOnceScriptType3=Vbs&WdacMode=Skip) för Windows 10.  

</br>  

<details>

<summary>Länkar till skriptet blir en saftig remsa. Klicka för att se exempel.</summary>

https://schneegans.de/windows/unattend-generator/?LanguageMode=Unattended&UILanguage=en-US&UserLocale=sv-SE&KeyboardLayout=041d%3A0000041d&GeoLocation=221&ProcessorArchitecture=amd64&ComputerNameMode=Random&TimeZoneMode=Implicit&PartitionMode=Unattended&PartitionLayout=GPT&EspSize=300&RecoveryMode=Partition&RecoverySize=1000&WindowsEditionMode=Unattended&WindowsEdition=pro&UserAccountMode=Unattended&AccountName0=Admin&AccountPassword0=password&AccountGroup0=Administrators&AccountName1=&AccountName2=&AccountName3=&AccountName4=&AutoLogonMode=Own&PasswordExpirationMode=Default&LockoutMode=Default&DisableSystemRestore=true&EnableLongPaths=true&HardenSystemDriveAcl=true&AllowPowerShellScripts=true&DisableLastAccess=true&NoAutoRebootWithLoggedOnUsers=true&TurnOffSystemSounds=true&DisableAppSuggestions=true&DisableWidgets=true&WifiMode=Interactive&ExpressSettings=DisableAll&Remove3DViewer=true&RemoveCalculator=true&RemoveCamera=true&RemoveClipchamp=true&RemoveClock=true&RemoveCopilot=true&RemoveCortana=true&RemoveDevHome=true&RemoveFamily=true&RemoveFeedbackHub=true&RemoveGetHelp=true&RemoveInternetExplorer=true&RemoveMailCalendar=true&RemoveMaps=true&RemoveMathInputPanel=true&RemoveNews=true&RemoveNotepadClassic=true&RemoveOneDrive=true&RemoveOneNote=true&RemoveOpenSSHClient=true&RemovePaint=true&RemovePaint3D=true&RemovePeople=true&RemovePhotos=true&RemovePowerAutomate=true&RemovePowerShellISE=true&RemoveQuickAssist=true&RemoveSkype=true&RemoveSnippingTool=true&RemoveSolitaire=true&RemoveStickyNotes=true&RemoveTeams=true&RemoveGetStarted=true&RemoveToDo=true&RemoveVoiceRecorder=true&RemoveWeather=true&RemoveWindowsMediaPlayer=true&RemoveZuneMusic=true&RemoveWindowsTerminal=true&RemoveWordPad=true&RemoveXboxApps=true&RemoveYourPhone=true&SystemScript0=&SystemScriptType0=Cmd&SystemScript1=&SystemScriptType1=Ps1&SystemScript2=&SystemScriptType2=Reg&SystemScript3=&SystemScriptType3=Vbs&DefaultUserScript0=&DefaultUserScriptType0=Reg&DefaultUserScript1=&DefaultUserScriptType1=Reg&DefaultUserScript2=&DefaultUserScriptType2=Reg&DefaultUserScript3=&DefaultUserScriptType3=Reg&FirstLogonScript0=&FirstLogonScriptType0=Cmd&FirstLogonScript1=&FirstLogonScriptType1=Ps1&FirstLogonScript2=&FirstLogonScriptType2=Reg&FirstLogonScript3=&FirstLogonScriptType3=Vbs&UserOnceScript0=&UserOnceScriptType0=Cmd&UserOnceScript1=&UserOnceScriptType1=Ps1&UserOnceScript2=&UserOnceScriptType2=Reg&UserOnceScript3=&UserOnceScriptType3=Vbs&WdacMode=Skip  

</details>  

</br>  

En volymlicensnyckel måste läggas till i skriptet för att en obevakad installation skall kunna genomföras. Leta upp raden "0000-0000-0000-0000" i autounattend.xml och ersätt den med W269N-WFGWX-YVC9B-4J6C9-T83GX, i detta fall en [volymlicensnyckel för Windows 10](https://learn.microsoft.com/en-us/windows-server/get-started/kms-client-activation-keys?tabs=server2025%2Cwindows10ltsc%2Cversion1803%2Cwindows81#windows-11-and-windows-10-semi-annual-channel) Pro.  

````xml  
<ProductKey>
    <Key>00000-00000-00000-00000-00000</Key>
</ProductKey>  
````  

</br>  

</br>  

En annan lösning är att ladda ner Windows genom [UUP dump](https://uupdump.net/) och välja senaste versionen och vad som skall ingå i ISO:n.

</br>  

</br>  

> [!TIPS]
> Om autounattend.xml läggs till som en egen ISO i samma VM som Windows ISO:n upptäcks skriptet och körs vid installationen. __Edit:__ Man kan nu ladda ner filen som ISO.

</br>  

> [!NOTERA]  
> Vid installation till VM kan man bli tvungen att logga in efter installationen, även om man har specat autologin i skriptet när Enhanced Session
> är aktiverad.  
