# Developing in Rust using Visual Studio Code
## Install related Visual Studio Code extensions
Install those 2 extensions:
  * Rust (rls) - For auto complete
  * CodeLLDB - For debugging
## Debugging the code
Create a launch.json using lldb
```javascript
{
  "version": "0.2.0",
  "configurations": [
    {
      "type": "lldb",
      "request": "launch",
      "name": "Launch",
      "args": [],
      "program": "${workspaceFolder}/target/debug/hello",
      "windows": {
        "program": "${workspaceFolder}/target/debug/hello.exe"
      },
      "cwd": "${workspaceFolder}",
      "stopOnEntry": false,
      "sourceLanguages": [
        "rust"
      ]
    }
  ]
}
```
  * To build: Press Ctrl + Shift + B
  * Toggle breakpoints: F9
  * To debug: Press F5
