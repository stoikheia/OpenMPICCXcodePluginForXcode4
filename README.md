OpenMPICCXcodePluginForXcode
=============================

OpenMPICC XcodePlugin for Xcode4.x, Xcode5.x

##Version

Version number in the plugin name "4.2" and "5.1" is LLVM version which used by openmpicc.


##Availabe Xcode Version

* Xcode4.x : Corresponding plugin is in OpenMPICCXcodePluginForXcode4 Folder.

* Xcode5.x : Corresponding plugin is in OpenMPICCXcodePluginForXcode5 Folder.

##USAGE

1. Install OpenMPI.

    e.g. installation by macports.

    ```
    $ sudo port install openmpi
    ```
    
    e.g. installation by homebrew.

    ```
    $ brew install openmpi
    ```


2. Check binary path.

    ```
    $ which openmpicc
    /opt/local/bin/openmpicc
    ```

    If path is not same to above, you should edit the .xcspec file of this project.
	(This example is for OpenMPICCXcodePluginForXcode4. If you want to use OpenMPICCXcodePluginForXcode5, you should change 4.2 to 5.1 below.)


    ```
    $vi OpenMPICC\ 4.2.xcplugin/Contents/Resources/OpenMPICC\ 4.2.xcspec
    ```

    Edit to path of line 33 to same as your environment.

    ```
    33    ExecPath = "/opt/local/bin/openmpicc";
    ```

    e.g. homebrew path

    ```
    33    ExecPath = "/usr/local/bin/mpicc";
    ```


3. Copy the plugin to Plug-ins directory. Plug-ins directory is a subfolder of Xcode Application Package.

    ```
    $ cp "OpenMPICC 4.2.xcplugin"  /Applications/Xcode.app/Contents/PlugIns/Xcode3Core.ideplugin/Contents/SharedSupport/Developer/Library/Xcode/Plug-ins/
    ```

4. Relaunch Xcode.

