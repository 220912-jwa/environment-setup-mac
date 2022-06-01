# mac-install-guide

## Install Using A Package Manager

A *package manager* is a command line tool that allows you to install and manage software. You can use a package manager to install all of the software listed here.

The package manager that we'll be using for this guide is called Homebrew. It's a command-line installer for MacOS, which means that you'll have to be running a macOS in order to use. If you are using a Windows machine the guide [here](https://github.com/210614-JavaFS/Enviroment-Setup) should be much more useful for you. The examples provided here are utilizing macvscodeOS Catalina version 10.15.5.

## Step 1: Install Homebrew
Go to Homebrew's [home page](https://brew.sh/) and copy the code seen in the image below.

<img src="./images/brew-1.png" width="500"/>

Open your terminal and type <code>brew</code>.

The result should look like the following:

<img src="./images/brew-2.png" width="300"/>

## Step 2: Install Git

With Homebrew installed, you are now ready to install Git. Open a terminal window and enter <code>brew install git</code>

To verify that Git is installed on your system, type <code>git --version</code>

## Step 3: Install JDK 11

I suggest installing java manually by following the instructions [here](https://docs.oracle.com/en/java/javase/11/install/installation-jdk-macos.html#GUID-2FE451B0-9572-4E38-A1A5-568B77B146DE) on Oracle's website.  

These steps may also work if you want to try through the command line: https://mkyong.com/java/how-to-install-java-on-mac-osx/


### Configure your Environment Variables
#### A. Mac OSX 10.5 or later:
In Mac OSX 10.5 or later, Apple recommends to set the <code>$JAVA_HOME</code> variable to <code>/usr/libexec/java_home</code>, just export <code>$JAVA_HOME</code> in file <code>~/. bash_profile</code> or ~<code>/.profile</code>.

```code
$ vim .bash_profile

export JAVA_HOME=$(/usr/libexec/java_home)

$ source .bash_profile

$ echo $JAVA_HOME
/Library/Java/JavaVirtualMachines/1.8.0.jdk/Contents/Home
```

#### B. Older Mac OSX:
For older Mac OSX, the <code>/usr/libexec/java_home</code> doesn’t exist, so, you should set <code>JAVA_HOME</code> to the fixed path:

```code
$ vim .bash_profile

export JAVA_HOME=/System/Library/Java/JavaVirtualMachines/1.8.0.jdk/Contents/Home

$ source .bash_profile

$ echo $JAVA_HOME
/System/Library/Java/JavaVirtualMachines/1.8.0.jdk/Contents/Home
```


## Step 4:  Install Eclipse IDE

1. Navigate to the [Eclipse Installer](https://www.eclipse.org/downloads/packages/installer) page and follow the instructions there for installing Eclipse IDE for Java EE Developers.

## Step 5: Install Maven

To install **Maven** with Homebrew, open your terminal window and run: <code>brew install maven</code> 

Once the download is complete, verify the installation by running: <code>mvn -v</code>

## Step 6: Install DBeaver

Navigate to https://dbeaver.io/download/ and download the appropriate version of DBeaver.

If your installation was successful, you should now be able to search for "dbeaver" in your spotlight with <code>cmd + space</code>.

## Step 7: Install Postman

The following is the single command required to install Postman on macOS using Homebrew:

<code>brew cask install postman</code>

## Step 8: Install Visual Studio Code

The following is the single command required to install Visual Studio Code on macOS using Homebrew:

<code>brew cask install visual-studio-code</code>

If you encounter problems and unable to install any of these applications with homebrew, refer to the manual download section of the [Environment Setup Guide](https://github.com/220531-jwa/environment-setup-windows) to install it manually instead. 


