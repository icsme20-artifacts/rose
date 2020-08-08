The minimum requirements for running the tools and scripts we developed for this work are described below. These steps were executed and tested using a fresh install of the Ubuntu 18.04 LTS environment. The approach relies on running an emulator, and some steps might take long to execute, although we paremeterize our scripts so it is not necessary to run the exact number of replications we executed for each experiment in the paper. Virtual machines might be unable to execute, since they might prevent running Android device emulators (we have used an Intel x86 image for the emulator device, which can't be executed inside an instance of a VirtualBox VM).

#### Install Java
Install OpenJDK 8:
```
sudo apt-get update && sudo apt-get install openjdk-8-jdk
```

#### Install Android Studio

Donwload the [Android Studio](https://developer.android.com/studio) .zip file.
Unzip at the `$HOME` folder, and manually install it by running the `studio.sh` script from the `bin` folder. 

#### Install stress-ng:
```
$ sudo apt-get update && sudo apt-get install stress-ng
```

#### Install required Python libraries:

We assume a working Python3 environment. We require installing the following libraries for executing the Minimal Hitting-Set (MHS) algorithm.
```
$ pip3 install python-sat
$ pip3 install numpy==1.16.1
```

#### Configure the SDK version and AVD from the command line (Android API version 28)
```
$ $HOME/Android/Sdk/tools/bin/sdkmanager "platforms;android-28"
$ $HOME/Android/Sdk/tools/bin/sdkmanager "system-images;android-28;default;x86"
$ $HOME/Android/Sdk/tools/bin/sdkmanager "build-tools;28.0.3" 
```

#### Create AVD device: 
```
$ $HOME/Android/Sdk/tools/bin/avdmanager create avd --name d --package "system-images;android-28;default;x86"
```

#### Download the apps:
To download the apps and use the exactly same commit that we used for each app, execute the following script:
```
$ ./install_apps.sh
```
This will create a folder called `projects` with all the projects used

#### Install the apps in AVD
Start the AVD:
```
$ emulator @d
```
Manually install the apps using Android Studio. Do so by opening each project and choosing to run any AndroidTest, this way it will install the app and tests into the emulator device.

#### Executing Shaker

This is all it takes for configuring the environment for running *Shaker* by using the predefined scripts for each research question from the paper, which are available at https://github.com/shaker-project/shaker.