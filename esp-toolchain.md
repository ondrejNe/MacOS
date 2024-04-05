#### ESP32 Toolchain Setup.sh
```sh
# !/bin/bash

# https://docs.espressif.com/projects/esp-idf/en/latest/esp32s3/get-started/linux-macos-setup.html

# Stop on the first sign of trouble
set -e

# Prerequisites
echo "Installing prerequisites..."
brew install cmake ninja dfu-util ccache python3

# ESP-IDF Setup
echo "Setting up ESP-IDF..."
mkdir -p esp
cd esp
git clone --recursive https://github.com/espressif/esp-idf.git

# Setup ESP-IDF
cd esp-idf
./install.sh esp32s3,esp32s2,esp32

# Set up the Environment Variables
echo "Setting up environment variables..."
. ./export.sh

# Append the environment variable setup to shell configuration files
echo ". $(pwd)/export.sh" >> ~/.bashrc
echo ". $(pwd)/export.sh" >> ~/.zshrc

echo "ESP-IDF setup is complete."
```
