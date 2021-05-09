# Fantasy Realms scoring app
Android scoring app for the game [FantasyRealms](https://boardgamegeek.com/boardgame/223040/fantasy-realms)

This app is a POC to learn android/kotlin.
Tested only on a Xiaomi red note 9.

Icon made by Freepik from www.flaticon.com

### Main features
- score calculation helper
- handle french and english (but any language can be implemented by adding new strings.xml file)
- card recognition through camera using [ML Kit](https://developers.google.com/ml-kit/vision/text-recognition/android). Only card titles required for recognition.

### Next steps : 
- In parameters menu, propose a testing screen for quick scanning + language option
- Decorate main activity
- add button to clear all hands ?

### About development
- During unit tests, if you encounter exception about version of Google service you have to install Play store
    * If ```Play Store``` is not available in your emulator, the only solution that I found is to manually update config.ini
    
``` 
For Windows, config.ini file can be found in : C:\Users\**YOURUSER**\.android\avd\**YOURDEVICE**.avd

Replace : 
 - "google_apis" by "google_apis_playstore" in the line starting by "image.sysdir.1=system-images..."
 - "PlayStore.enabled=false" by "PlayStore.enabled=true"
 - "tag.id=google_apis" by "tag.id=google_apis_playstore"

Open "AVD manager" in IDE and redownload...
```
