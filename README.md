# AdoptOpenJDK-jre-11.0.5-DCEVM

The files in this project are Java Runtime Environments from [AdoptOpenJDK](https://adoptopenjdk.net/index.html?variant=openjdk11&jvmVariant=hotspot) with the [DCEVM](http://dcevm.github.io/) from [TravaJDK](https://github.com/TravaOpenJDK) added

To use the DCEVM JRE, point to it to be used by your application as a JRE. While your application is running you can make changes to it and then see those changes take effect by recompiling the changed classes.

There is also some example Java code here to illustrate what DCEVM can do, the java example can be run as a Console Application. This sample code mimics an application server, it has a 30 second start up, and 5 minute run time. Here you can make changes and watch the "log activity" reflect those changes. Don't forget to point to the DCEVM JRE, and to recompile your classes!

In order to make this DCEVM JRE I copied the JVM file from [Trava JDK 11 ](https://github.com/TravaOpenJDK/trava-jdk-11-dcevm) into the [AdoptOpenJDK's JRE v 11.0.5](https://adoptopenjdk.net/archive.html?variant=openjdk11&jvmVariant=hotspot), I also added the modules file from AdoptOpenJDK 11.0.5 into the JRE.

To replicate what I did here are the steps you need to take

## Windows
  1. [Download AdoptOpenJDK's JRE version 11.0.5](https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_windows_hotspot_11.0.5_10.zip)
  2. [Download AdoptOpenJDK 11.0.5](https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_windows_hotspot_11.0.5_10.zip)
  3. [Download TravaJDK 11.0.5](https://github.com/TravaOpenJDK/trava-jdk-11-dcevm/releases/download/dcevm-11.0.5%2B5/java11-openjdk-dcevm-windows.zip)
  4. Extract all downloaded files
  5. Copy {TravaJDK Directory}/bin/server/jvm.dll to {JRE Directory}/bin/server/jvm.dll
  6. Copy {AdoptOpenJDK Directory}/lib/modules to {JRE Directory}/lib/modules
  
## OSX
  1. [Download AdoptOpenJDK's JRE version 11.0.5](https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jre_x64_mac_hotspot_11.0.5_10.tar.gz)
  2. [Download AdoptOpenJDK 11.0.5](https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/download/jdk-11.0.5%2B10/OpenJDK11U-jdk_x64_mac_hotspot_11.0.5_10.tar.gz)
  3. [Download TravaJDK 11.0.5](https://github.com/TravaOpenJDK/trava-jdk-11-dcevm/releases/download/dcevm-11.0.5%2B5/java11-openjdk-dcevm-osx.tar.gz)
  4. Extract all downloaded files, to open the extracted files you may need to right click and select "Show Package Contents"
  5. Copy {TravaJDK Directory}/Contents/Home/lib/server/libjvm.dylib to {JRE Directory}/Contents/Home/lib/server/libjvm.dylib 
  6. Copy {AdoptOpenJDK Directory}/Contents/Home/lib/modules to {JRE Directory}/Contents/Home/lib/modules

### Licensing Information
This project is licensed under the [Apache License v2](https://www.apache.org/licenses/LICENSE-2.0)

TravaJDK license information can be viewed here: https://github.com/TravaOpenJDK/trava-jdk-11-dcevm/blob/master/LICENSE

AdoptOpenJDK license information can be viewed here: https://adoptopenjdk.net/about.html?variant=openjdk11&jvmVariant=hotspot
