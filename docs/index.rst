.. _lib.aws.greengrass:

**************
AWS Greengrass
**************

`AWS Greengrass <https://aws.amazon.com/greengrass/>`_ lets you build IoT solutions that connect different types of devices with the cloud and each other. Devices that run Linux and support ARM or x86 architectures can host the Greengrass Core. The Greengrass Core enables the local execution of AWS Lambda code, messaging, data caching, and security.

Devices running AWS Greengrass Core act as a hub that can communicate with other devices able to connect to AWS IoT Core, such as microcontroller based devices or large appliances.

AWS Greengrass Core devices and the AWS IoT Core devices can be configured to communicate with one another in a Greengrass Group. If the Greengrass Core device loses connectivity to the cloud, devices in the Greengrass Group can continue to communicate with each other over the local network. A Greengrass Group may represent one floor of a building, one truck, or an entire mining site.

The Zerynth AWS Greengrass Library extends :ref:`Zerynth AWS IoT Core Library <lib.aws.iot>` with functions to retrieve info about an AWS Greengrass Core:

.. include:: __toc.rst