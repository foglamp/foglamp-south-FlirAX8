cmake_minimum_required(VERSION 2.4.0)

# Set the plugin name to build
project(FlirAX8)

# Supported options:
# -DFLEDGE_INSTALL
#
# Set plugin type (south, north, filter)
set(PLUGIN_TYPE "south")

# Find source files
file(GLOB JSON_FILES *.json)

set(FLEDGE_INSTALL "" CACHE INTERNAL "")
# Install library
if (FLEDGE_INSTALL)
        message(STATUS "Installing ${PROJECT_NAME} in ${FLEDGE_INSTALL}/plugins/${PLUGIN_TYPE}/${PROJECT_NAME}")
        install(FILES ${JSON_FILES} DESTINATION ${FLEDGE_INSTALL}/plugins/${PLUGIN_TYPE}/${PROJECT_NAME})
endif()

