# Project Properties
####################
CMAKE_MINIMUM_REQUIRED (VERSION 2.6.2)
PROJECT(led_controller)
# This will be extended to take the version from SCM
# Version config can be simplified from 3.0+
SET(led_controller_VERSION_MAJOR 0)
SET(led_controller_VERSION_MINOR 9)
SET(led_controller_VERSION_PATCH 1)
SET(led_controller_VERSION
    ${led_controller_VERSION_MAJOR}.${led_controller_VERSION_MINOR}.${led_controller_VERSION_PATCH})

# Options
###################
SET(CMAKE_VERBOSE_MAKEFILE 1)
SET(CMAKE_BUILD_TYPE DEBUG) # Options MINSIZEREL, RELEASE, DEBUG

# Paths
########
ADD_SUBDIRECTORY(src)
