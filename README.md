# Cucumber Android Example Project (POM)
This is a example project to automated android native app. 

### Pre-requisite/s software installed
1. Git
2. Eclipse
3. Docker

### Athena installation Steps
1. Clone athena repo to your home directory: <br>
```$ git clone https://github.com/athena-oss/athena.git``` <br>
``` - go to athena root dir using terminal (ex. cd athena/)``` <br>
``` execute ./athena init ``` <br>
``` - Follow the ATHENA instruction to make ATHENA global``` <br>
``` - Restart your terminal ``` <br>
<b>OR Add following to bash_profile</b><br>
```a. $ vi ~/.bash_profile``` (Mac User) , ```vi ~/.bashrc``` (Linux User) <br>
```b. add the following at the end of line``` <br>
      ```export ATHENA_HOME=/<installation location>/athena``` <br>
      ```export PATH=${PATH}:$ATHENA_HOME```
2. execute again ```$ athena init``` under athena project to check if athena is properly installed

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
