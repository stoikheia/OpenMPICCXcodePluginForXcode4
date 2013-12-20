OpenMPICCXcodePluginForXcode4
=============================

OpenMPICC XcodePlugin for Xcode4.x

##Version

Version number in the plugin name "4.2" is LLVM version which used by openmpicc.

##USAGE

1. Install OpenMPI.

    e.g. installation by macports.

    ```
    $ sudo port install openmpi
    ```


2. Check binary path.

    ```
    $ which openmpicc
    /opt/local/bin/openmpicc
    ```

    If path is not same to above, you should edit the .xcspec file of this project.

    ```
    $vi OpenMPICC\ 4.2.xcplugin/Contents/Resources/OpenMPICC\ 4.2.xcspec
    ```

    Edit to path of line 33 to same as your environment.
    ```
    33    ExecPath = "/opt/local/bin/openmpicc";
    ```

3. Copy the plugin to Plug-ins directory. Plug-ins directory is a subfolder of Xcode Application Package.

    ```
    $ cp "OpenMPICC 4.2.xcplugin"  /Applications/Xcode.app/Contents/PlugIns/Xcode3Core.ideplugin/Contents/SharedSupport/Developer/Library/Xcode/Plug-ins/
    ```

4. Relaunch Xcode.

