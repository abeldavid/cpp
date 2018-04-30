# cpp

Use this template to run C++ files.

Edit the following files :

In **tasks.json**

{
    "version": "2.0.0",
    "tasks": [
        {
            "label": "**label ur file** ",
            "type": "shell",
            "command": "g++",
            "args": [
                "-g", " **nameofurfile** .cpp"
            ],
            "group": {
                "kind": "build",
                "isDefault": true
            }
        }
    ]
}

In **launch.json**

{
    // Use IntelliSense to learn about possible attributes.
    // Hover to view descriptions of existing attributes.
    // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
    "version": "0.2.0",
    "configurations": [
        {
            "name": "(gdb) Launch",
            "type": "cppdbg",
            "request": "launch",
            "program": "${workspaceFolder}**/cpp_filename.exe**",
            "args": [],
            "stopAtEntry": false,
            "cwd": "${workspaceFolder}",
            "environment": [],
            "externalConsole": true,
            "MIMode": "gdb",
            "miDebuggerPath": "C:\\MinGW\\bin\\gdb.exe",
            "preLaunchTask": "**label ur file**",
            "setupCommands": [
                {
                    "description": "Enable pretty-printing for gdb",
                    "text": "-enable-pretty-printing",
                    "ignoreFailures": true
                }
            ]
        }
    ]
}
