# Cucumber Android Example Project (POM)
This is a example project to automated android native app. 

### Pre-requisite/s software installed
1. Git
2. Eclipse
3. Docker

<b>Steps To Run Example Tests:</b>
Note: Start the genymotion virtual device (Samsung Galaxy S6)
1. Clone this repository to your home directory
2. Start the selenium hub (command: athena selenium start hub 2.53.1)
3. Start the appium (athena appium start --apks-dir=cucumber_android/apps --adb-port=5037)
4. Execute the example tests (athena appium java example-tests/java clean test)

<b>Add info:</b> There are instance that virtual device/s not automatically connect, you can follow the steps below to check if there is connected devices
1. execute "athena appium terminal". You will be inside the appium container.
2. execute "adb devices" to check if there is connected devices
3. execute to connect a devices "adb connect <IP of Genymotion> :5555" (ex. adb connect 192.168.60.101:5555), IP of genymotion devices usually display on top
4. type "exit" and run again the tests
  
<b>Youtube Link:</b> https://youtu.be/R-PL2GeRc04
