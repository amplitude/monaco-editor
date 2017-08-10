# monaco
Compiled version of Amplitude fork of Microsoft's ```monaco-editor```.
Pieced together from [this guide](https://github.com/Microsoft/monaco-editor/blob/master/CONTRIBUTING.md).

## setup
Instructions for modifying the ```vscode``` source code and regenerating these files.

1. Clone the Amplitude forks of ```vscode``` and ```monaco-editor``` _in the same directory_.
1. [Make sure you're not using NPM 5](https://github.com/Microsoft/vscode/issues/30134): ```npm install -g npm@4.6.1```
1. Install ```vscode``` dependencies: ```vscode> ./scripts/npm.sh install```
1. Start the ```vscode``` compiler: ```vscode> npm run watch```
1. Make any changes you'd like to make to the ```vscode``` source 
1. Bump the version up in ```vscode/build/monaco/package.json```.
1. Build the editor source ```vscode> node_modules/.bin/gulp editor-distro```
1. Bump the version up in ```monaco-editor/package.json```.
1. Fetch monaco-editor dependencies: ```monaco-editor> npm install .```
1. Build the monaco-editor package ```npm run release```
1. Copy the distro you want from ```monaco-editor/release/```
1. But don't forget to keep this README here (```/src/static/js/monaco/```)

