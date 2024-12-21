
#  ADB AND AVD 
    => These are used to debug the application on run time.
    => ADB :- Android debug bridge. (Runs on Real/virtual device)
    => AVD :- Android virtual device.

    AVD (Android Virtual Device) and ADB (Android Debug Bridge) are tools used in Android development, each serving different purposes:
    AVD (Android Virtual Device):
            AVD refers to a configuration that allows developers to emulate an Android device on their computer using the Android Emulator.
            It is part of Android Studio, enabling testing and debugging of Android applications without needing a physical device.
            Developers can specify various parameters for an AVD, such as:
            Screen size and resolution.
            Android version (API level).
            Hardware features (e.g., RAM, storage, GPU).
        Example Use:
        To test how an app behaves on different screen sizes or Android versions.

    ADB (Android Debug Bridge):
        ADB is a command-line tool that allows developers to communicate with Android devices (real or virtual) from their computer.
            It acts as a bridge between a development machine and an Android device/emulator.
            Functions include:
            Installing/uninstalling apps.
            Accessing device logs.
            Debugging apps.
        Transferring files between the development machine and the device.
        # Common ADB Commands:
            adb devices - Lists connected devices/emulators.
            adb install app.apk - Installs an APK file on the connected device.
            adb logcat - Shows the device's log messages.
            adb shell - Opens a shell on the connected device for advanced debugging or configuration.
            Both tools are essential for Android developers to streamline the development and testing process.

            adb devices
            Lists all connected devices or emulators.
            Output includes the device ID and status (e.g., device, offline, or unauthorized).
            adb version

            Displays the version of ADB installed.
            adb help

            Shows help information about ADB commands.
            
            App Management
            adb install <path/to/app.apk>

            Installs an APK file on the connected device.
            Add the -r flag to reinstall without uninstalling the app:
            adb install -r app.apk
            adb uninstall <package_name>

            Uninstalls an app from the device.
            adb shell pm list packages

            Lists all installed packages on the device.
            Add filters:
            -3: Third-party apps.
            -s: System apps.
            adb shell am start -n <package_name>/<activity_name>

            Launches an app/activity.
            File Operations
            adb push <local_path> <remote_path>

            Copies a file from the computer to the device.
            Example: adb push myfile.txt /sdcard/
            adb pull <remote_path> <local_path>

            Copies a file from the device to the computer.
            Example: adb pull /sdcard/myfile.txt ./
            adb shell ls <path>

            Lists files and directories in the specified path on the device.
            Debugging and Logs
            adb logcat

            Streams the device's log output.
            Add filters, such as adb logcat *:E (only errors).
            adb shell dumpsys

            Provides system diagnostics and information.
            adb bugreport <output_file>

            Generates a bug report for the connected device.
            Device Control
            adb reboot

            Reboots the device.
            adb reboot recovery

            Reboots the device into recovery mode.
            adb shell

            Opens a shell session to execute Linux commands directly on the device.
            adb emu <command>

            Sends commands to an emulator.
            Example: adb emu kill (stops the emulator).
            Network Commands
            adb tcpip <port>

            Enables ADB over TCP/IP on the specified port.
            Example: adb tcpip 5555
            adb connect <ip_address:port>

            Connects to a device/emulator over a network.
            Example: adb connect 192.168.1.100:5555
            adb disconnect <ip_address:port>

            Disconnects from a device/emulator.
            Screen and Input
            adb shell screencap <path>

            Captures a screenshot.
            Example: adb shell screencap /sdcard/screen.png
            adb shell screenrecord <path>

            Records the device’s screen.
            Example: adb shell screenrecord /sdcard/demo.mp4
            adb shell input text "<text>"

            Simulates typing text on the device.
            adb shell input keyevent <key_code>

            Simulates a key press.
            Example: adb shell input keyevent 26 (power button).
            Advanced Commands
            adb root

            Restarts ADB with root permissions (if the device allows).
            adb shell settings get <namespace> <key>

            Gets a specific setting value.
            Example: adb shell settings get system screen_brightness
            adb shell settings put <namespace> <key> <value>

            Updates a setting value.
            Example: adb shell settings put system screen_brightness 200
            Examples for Common Scenarios:
            Check Internet Connectivity:
            adb shell ping -c 4 google.com

            Clear App Data:
            adb shell pm clear <package_name>

            View Device Info:
            adb shell getprop
