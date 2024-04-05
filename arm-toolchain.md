#### Tap the repository

```sh
brew tap osx-cross/arm
```

#### Install the toolchain
```sh
brew install arm-gcc-bin
brew install --cask gcc-arm-embedded

brew tap discoteq/discoteq
brew install flock
brew install x86_64-elf-gcc  # Used by simulator
brew install u-boot-tools  # Some platform integrate with u-boot
```

https://nuttx.apache.org/docs/latest/quickstart/install.html#prerequisites
