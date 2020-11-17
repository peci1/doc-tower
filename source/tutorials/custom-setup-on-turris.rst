######################
Custom Setup on Turris OS 5.x and newer
######################

If you need more permanent solution than **HARDWARIO Playground** you can install all the services yourself in your system.
This guide will help you to install and configure these services:

- HARDWARIO Gateway ``bcg``
- HARDWARIO Firmware Tool ``bcf``
- HARDWARIO Host Tool ``bch``

.. _turris-instalation:

************
Installation
************

Step 1: Update the package
**************************

.. code-block:: console

    opkg update

Step 2: Install the BigClown tools
***********************************************************************************

.. code-block:: console
    :linenos:

    opkg install bigclown-control-tool bigclown-firmware-tool bigclown-gateway

***************************************
Finishing for Radio Dongle as a gateway
***************************************

Follow these steps if you have `Radio Dongle <https://shop.hardwario.com/radio-dongle/>`_ as a gateway.

Step 1: Finish :ref:`installation <turris-instalation>` part
************************************************************

Step 2: Make sure the configuration works
*****************************************

.. code-block:: console

    uci show bigclown-gateway

Step 3: Enable service for gateway
**********************************

.. code-block:: console

    /etc/init.d/bigclown-gateway enable

Step 4: Start service
*********************

.. code-block:: console

    /etc/init.d/bigclown-gateway start
