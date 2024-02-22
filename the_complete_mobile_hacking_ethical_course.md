# The Complete Mobile Ethical Hacking Course

## Resources
- https://github.com/ec-council-learning/The-Complete-Mobile-Ethical-Hacking
- http://pallergabor.uw.hu/androidblog/dalvik_opcodes.html
- Mobile apps
    - https://github.com/atilsamancioglu/MS2-WordGame
- Decompilers
    - https://dedexer.sourceforge.net/
    - https://www.decompiler.com/
    - https://jdec.app/
    - https://dogbolt.org/
- Software
    - ngrok

- Backdoor Android vs iOS
    - Apple App store requires 100$ developer account, but each app is verified before being published
    - Android one can run untrusted software and publish to the app store quite easily
- Payload
    - Generate it with MSFVenom
    - Generates a payload with meterpreter session (or other)
        - `msfvenom -p andoid/meterpreter/reverse_tcp`
        - requires a remote host and port to connect back to
            - This is hosted using ngrok which exposes a web service and forwards the traffic to your host machine
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
    

