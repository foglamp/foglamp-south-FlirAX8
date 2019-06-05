================================
South plugin for Flir AX8 camera
================================

A plugin that connects a Flir AX8 camera via Modbus TCP.

This plugin consists of the modbus map for the camera and will
load the gneric modbus-c plugin to provide the connectivity layer.

Description
-----------

This plugin supports FlirAX8 device connected via modbus interface. It internally
uses foglamp-south-modbusc plugin and Linux libmodbus library.


Build
-----

To build FlirAX8 modbus plugin run the commands:

.. code-block:: console

  $ mkdir build
  $ cd build
  $ cmake ..
  $ make

You may also pass following option to cmake to override 
the default behaviour:

- **FOGLAMP_INSTALL** sets the installation path of this plugin

NOTE:
 - 'make install' target is defined only when **FOGLAMP_INSTALL** is set

Examples:

- no options

  $ cmake ..

- no options and FOGLAMP_ROOT set

  $ export FOGLAMP_ROOT=/some_foglamp_setup

  $ cmake ..

- set FOGLAMP_INSTALL

  $ cmake -DFOGLAMP_INSTALL=/home/source/develop/FogLAMP

  $ cmake -DFOGLAMP_INSTALL=/usr/local/foglamp
