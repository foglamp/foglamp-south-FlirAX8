cmake_minimum_required(VERSION 2.4.0)

# Set the plugin name to build
project(FlirAX8)

# Supported options:
# -DFOGLAMP_INSTALL
#
# Set plugin type (south, north, filter)
set(PLUGIN_TYPE "south")

# Find source files
file(GLOB JSON_FILES *.json)

set(FOGLAMP_INSTALL "" CACHE INTERNAL "")
# Install library
if (FOGLAMP_INSTALL)
        message(STATUS "Installing ${PROJECT_NAME} in ${FOGLAMP_INSTALL}/plugins/${PLUGIN_TYPE}/${PROJECT_NAME}")
        install(FILES ${JSON_FILES} DESTINATION ${FOGLAMP_INSTALL}/plugins/${PLUGIN_TYPE}/${PROJECT_NAME})
endif()

