# VSCode settings

* Extensions
    * Python
    * Monokai pro (Filter Spectrum)
    * Remote ssh
    * Python
    * Prettier
* Keybindings
    * Go to Definition: ctrl + (
    * Go back to code: ctrl + -
    * Close tab: cmd + w (Same as MAC)
    * Open file: cmd + o (Same as MAC)


## Cursor

* Disable file watcher: https://claude.ai/code/artifact/7e22a98c-da29-4774-ad27-75ef1c945bfa

## Debugging

* Use command palette to start debugger

### launch.json
```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "name": "Python Debugger: Current File",
            "type": "debugpy",
            "request": "launch",
            "cwd": "${workspaceFolder}",
            "program": "run.py",
            "console": "integratedTerminal",
            "args": [
                "--skip-phase0",
                "--config",
                "configs/config.yaml"
            ]
        }
    ]
}
```
