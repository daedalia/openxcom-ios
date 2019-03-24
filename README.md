# OXCE for iOS
A repository with everything needed to build OXCE (OpenXcom Extended) for iOS.

## Getting the source code
Some of the projects (including OpenXcom) are added via submodules. In order to retrieve them, you have to instruct `git` to
get them along with the rest of the repository. The easiest way to do that is to just clone the repository recursively:

    $ git clone --recursive https://github.com/MeridianOXC/openxcom-ios

If your git client doesn't support recursive cloning, you can clone the repository and then initialize the submodules manually:

    $ git clone https://github.com/MeridianOXC/openxcom-ios
    $ cd openxcom-ios
    $ git submodule update --init --recursive
    
## Building the app
Go to `Sources/OpenXcom/xcode-ios` and open the `OpenXcom.xcodeproj` project file. This should open your Xcode, with
all subprojects and resources in place. Be sure to configure your signing certificate before running on a real device!

You may want to place your *X-Com: UFO Defense* and/or *Terror from the Deep* files into `Sources/OpenXcom/bin/UFO` and
`Sources/OpenXcom/bin/TFTD` folders respectively. This will copy the game data into the app bundle, which will allow you
to run OpenXcom a lot more easily. Note though that this *will make the app bundle non-redistributable*! Not like there's
a way to redistribute an app outside of an app store anyway.

## Running the app on iOS
If you copied your *UFO Defense*/*TFTD* files into the bundle during the build phase, that's probably everything you'd want.
If not, you'll be greeted with an error message upon running the app. This means you'll have to use iTunes to get the data
to the app: you'll have to copy your `UFO` and/or `TFTD` folder from a working installation of OpenXcom.

Saved games are in the xcom1 and xcom2 folders that you can access via iTunes. They should be compatible with the desktop
versions.

Mods can also be uploaded via iTunes. For easier handling of big mods, it is recommended to use OXCE's ziploader.

## Credits
This is a fork of sfalexrog's repository of OpenXcom for iOS and most of the actual work has been done by him.

I (Meridian) have only copied and customized his work on this build system.
