# Installing Homebrew on Mac

## What is homebrew?

**Homebrew** is a free and open-source software package management system that simplifies the installation of software on Apple's operating system, macOS, as well as Linux. The name is intended to suggest the idea of building software on the Mac depending on the user's taste.

## What Does Homebrew Do?

* Homebrew installs **the stuff you need** that Apple (or your Linux system) didn’t.
    
* It makes installing lots of different software like Git, Ruby, and Node simpler.
    
* It lets you avoid possible security problems associated with using the `sudo` command to install the software.
    
* `To install, drag this icon…` no more. Homebrew Cask installs macOS apps, fonts and plugins and other non-open source software.
    

## Prerequisites

* **You should have some familiarity with the Mac Terminal application** since you’ll need to use it to install Homebrew. The Terminal application is located in the Utilities folder in the Applications folder. Alternatively, you can press ⌘ + space to open up the spotlight & search for the terminal.
    
* **Dependencies.** You need to install one other piece of software before you can install Homebrew:
    
* **Xcode.** Install Apple’s Xcode development software: [Xcode in the Apple App Store](http://itunes.apple.com/us/app/xcode/id497799835?ls=1&mt=12).
    

## How to Install Homebrew

* Open the Terminal app & type either one of these commands:
    
* ```bash
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    
    # OR
    # If you want to run the Homebrew installer non-interactively without prompting for passwords (e.g. in automation scripts), you can use:
    NONINTERACTIVE=1 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```
    

* The **interactive** script explains what it will do and then pauses before it does it. Read about other [installation options](https://docs.brew.sh/Installation).
    

## How to Update Homebrew

New versions of Homebrew come out frequently, so make sure you update it before updating any of the other software components that you’ve installed using Homebrew.

* In Terminal type `brew update`
    
* ```bash
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/uninstall.sh)"
    
    # & If you want to run the Homebrew uninstaller non-interactively, you can use: 
    NONINTERACTIVE=1 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/uninstall.sh)"
    ```
    

## How to Uninstall Homebrew

* Open the Terminal app
    
* ```bash
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/uninstall.sh)"
    
    
    #If you want to run the Homebrew uninstaller non-interactively, you can use:
    NONINTERACTIVE=1 /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/uninstall.sh)"
    ```
    

* This downloads and runs the uninstaller script. Follow the instructions and Homebrew will be removed from your computer.
    

**Last but not least**, refer to this [official github page](https://github.com/Homebrew/install#homebrew-uninstaller) for latest information about how to install & uninstall Homebrew.