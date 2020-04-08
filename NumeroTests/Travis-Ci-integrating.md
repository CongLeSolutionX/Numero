#  Use Travis for CI 

Open terminal, navigate into the working directory
Creat a new hidden yml file and open it with TextEdit
```zsh 
touch .travis.yml
open -a TextEdit .travis.yml
```
Add these lines to the file into the .travis.yml 

```
osx_image: xcode10.2
language: swift
os: osx
xcode_project: Numero.xcodeproj
xcode_scheme: Numero
xcode_destination: platform=iOS Simulator,OS=12.2,name=iPhone 8

```

The first three lines tell Travis CI to use Xcode 10.2, Swift and macOS to build and run your project. 
The default macOS version for this Xcode is 10.14.
Check the Travis CI macOS Build Environment: [macOS Version page for updates](https://docs.travis-ci.com/user/reference/osx/#macos-version).

The last three lines specify the .xcodeproj file to run, the name of the scheme, and where you want Travis CI to run the project.
In this case, we are using the iOS simulator, running iOS 12.2 on an iPhone 8. 

Save .travis.yml, then commit and push your changes to GitHub
