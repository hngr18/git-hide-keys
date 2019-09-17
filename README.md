# git-hide-keys
Hide sensitive API keys and secrets without having to add them to environment variables (for Linux only currently)

This was written for and tested with repositories with JSON config files

## How it works
- Ensure you have jq library installed
- Clone this repository
- Take the git-hide-keys file and put it into a directory that is included within your PATH environment variable or add the folder git-hide-keys in to the PATH environment variable
- Add a .hide file to the repository

## .hide file format
### filepath=jq expression
- test.json=.contributes.configuration.properties.configKey.default
- nested/test.json=.contributes.configuration.properties.configKey.default
- vscode-translator/package.json=.contributes.configuration.properties."translation.apiKey".default
