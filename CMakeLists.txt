# Project Properties
####################
CMAKE_MINIMUM_REQUIRED (VERSION 2.6.2)
PROJECT(button_led_controller)
# This will be extended to take the version from SCM
# Version config can be simplified from 3.0+
SET(button_led_controller_VERSION_MAJOR 0)
SET(button_led_controller_VERSION_MINOR 9)
SET(button_led_controller_VERSION_PATCH 1)
SET(button_led_controller_VERSION
    ${button_led_controller_VERSION_MAJOR}.${button_led_controller_VERSION_MINOR}.${button_led_controller_VERSION_PATCH})

# Options
###################
SET(CMAKE_VERBOSE_MAKEFILE 1)
SET(CMAKE_BUILD_TYPE DEBUG) # Options MINSIZEREL, RELEASE, DEBUG

# Paths
########
ADD_SUBDIRECTORY(src)
