#  Using command line for Unit tests 


Point xcode-select to the Xcode App Developer directory using the command: 
```zsh 
sudo xcode-select -s /Applications/Xcode.app/Contents/Developer
```
Now, run the fowwlong command to start the unit tests
```zsh
xcodebuild -project 'Numero.xcodeproj' -scheme 'Numero' -destination 'platform=iOS Simulator,name=iPhone 8' test | xcpretty
```
