# exeggcute
List of commands to free up space on your MacOS machine used for development.

Also includes not-development commands (ej. Spotify, Chrome...)

## Commands
USE AT YOUR OWN RISK. This commands are not risky, but anyway you should check carefully what each of them does in order to not prevent surprises.

```
brew update
brew upgrade
brew cleanup
gem update
gem cleanup
pod cache clean --all
rm -rf ~/Library/Caches/CocoaPods
xcrun simctl delete unavailable
rm -rf ~/Library/Developer/Xcode/Archives
rm -rf ~/Library/Developer/Xcode/DerivedData
rm -rf ~/Library/Developer/Xcode/iOS Device Logs/
rm -rf ~/Library/Developer/CoreSimulator/
rm -rf ~/Library/Developer/Xcode/iOS\ DeviceSupport
rm -rf ~/Library/Caches/com.apple.dt.Xcode
rm -rf ~/Library/Caches/AndroidStudio3.6
find . -name "node_modules" -type d -mtime +120 | xargs rm -rf
npm install -g npm
rm -rf ~/Library/Caches/com.spotify.client
rm -rf ~/Library/Application\ Support/Spotify/PersistentCache/mercury.db
rm -rf ~/Library/Application\ Support/Microsoft/Skype\ for\ Desktop/Cache
rm -rf ~/Library/Caches/Google/Chrome
```

### Extra commands
```
brew cask upgrade
brew doctor
delete /android/avd/<emulator>/snapshots/default_boot/…
rbenv uninstall <version>
```

## Commands explained

### Brew

#### brew update
Updates Homebrew itself.

#### brew upgrade
Upgrade your Homebrew-installed software to their latest versions.

#### brew cleanup
Uninstalls old versions of a formula.

### RubyGems

#### gem update
Update installed gems to the latest version.

#### gem cleanup
Clean up old versions of installed gems.

### Xcode

#### pod cache clean --all
Clears CocoaPods cache.

#### rm -rf ~/Library/Caches/CocoaPods
Clears CocoaPods cache if any still present.

#### xcrun simctl delete unavailable
Clears unneeded Xcode simulators.

#### rm -rf ~/Library/Developer/Xcode/Archives
Clears Xcode archives.

#### rm -rf ~/Library/Developer/Xcode/DerivedData
Clears Xcode DerivedData (intermediate build results, generated indexes)

#### rm -rf ~~/Library/Developer/Xcode/iOS Device Logs/
Clears Xcode Devices logs.

#### rm -rf ~/Library/Developer/CoreSimulator/
Clears user data present in Simulators.

#### rm -rf ~/Library/Developer/Xcode/iOS\ DeviceSupport
Clears Xcode symbolicate crash logs.

#### rm -rf ~/Library/Caches/com.apple.dt.Xcode
Clears, amongs others, a variety of disk images for various versions of OS documentation.

### Android Studio

#### rm -rf ~/Library/Caches/AndroidStudio3.6
Clears Android Studio cache.

### NPM & Node Modules

#### find . -name "node_modules" -type d -mtime +120 | xargs rm -rf
Clears outdated node modules.

#### npm install -g npm
Updates NPM packages.

### Misc

#### rm -rf ~/Library/Caches/com.spotify.client
Clears Spotify cache.

#### rm -rf ~/Library/Application\ Support/Spotify/PersistentCache/mercury.db
Clears Spotify Persistent cache.

#### rm -rf ~/Library/Application\ Support/Microsoft/Skype\ for\ Desktop/Cache
Clears Skype cache.

#### rm -rf ~/Library/Caches/Google/Chrome
Clears Google Chrome cache.

### Optional

#### brew cask upgrade
Upgrade your Homebrew Cask installed software to their latest versions.

#### brew doctor
Warns about issues with your Homebrew installation and packages.

#### delete /android/avd/{emulator}/snapshots/default_boot/
Deletes Android `{emulator}`.

#### rbenv uninstall {version}
Removes Ruby `{version}`.
