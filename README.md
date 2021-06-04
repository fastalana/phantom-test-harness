# phantom-test-harness
Test harness was created to make building Phantom apps a better experience. This project includes:
* a dummy BaseConnector
* Vault
* An ActionResult module
* phantom.app
* phantom.ph_utils
* phantom.cef

Each module has been optimized to best of my ability for test and debug.

# Why use this?
This test harness decouples Phantom App development from the Phantom platform. This allows you to develop and test new and existing apps on your own machine withouth having to worry about Phantom platform dependencies. Yes, you can put "print" statements all over your code again, like a true Python programmer :)

It is important to note, that while this is a handy tool for app development it does not connect to Phantom or test any Phantom platform code.

# Logging
Activity is logged to a file and to the console by default. The log file location is the current location of execution, unless otherwise specified (BaseConnector - log_path). Console logging can be disabled as well (BaseConnector - log_to_console)

# How to use
1. Clone this repo
2. Add the location of this project to your PYTHONPATH
```export PYTHONPATH=$PYTHONPATH:/your/new/location/phantom-test-harness```
3. Make sure you run your python code that tests your app from somewhere that you can import your app module from. It's recommended to test from withing your app code directory.
4. Check `/examples` for examples on how to use this.

# Options

There are a lot of options that you can use depending on your scenario. Some options are strictly for debugging purposes, and some are for making sure that your app doesn't break. Options are defined in `BaseConnector.py:init()`. There are comments as to which each are for. Some probably need more clarity. Please see examples for some ideas of how to use and access these.

# Examples
Examples of usage can be found in the `/examples` folder for this project.

# Other important stuff

This is very alpha. If you run into BaseConnector methods, or other things that haven't been implemented, please feel free to open an issue or a PR.
