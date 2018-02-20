.. module:: greengrass

**************************************
Amazon Web Services Greengrass Library
**************************************

The Zerynth AWS Greengrass Library contains helper functions for IoT devices to retrieve info about an `AWS Greengrass Core <https://aws.amazon.com/greengrass/>`_.


.. note:: to connect to an AWS Greengrass Core after info retrieval use :ref:`Zerynth AWS IoT Core Library <lib.aws.iot>`

    
=======================
The DiscoveryInfo class
=======================

.. class:: DiscoveryInfo(raw_info)

        A DiscoveryInfo instance is returned by :func:`greengrass.discover` function.

        It exposes the following attributes and methods:

            * :attr:`DiscoveryInfo.raw` dictionary containing raw `discovery response <https://docs.aws.amazon.com/greengrass/latest/developerguide/gg-discover-api.html#gg-discover-response-doc>`_.
            * :meth:`DiscoveryInfo.CA`
            * :meth:`DiscoveryInfo.connectivity`

    
.. method:: CA()

    Returns Greengrass Core CA Certificate if only one Server Certificate is returned by discover call.
    Raises :code:`GreengrassDiscoveryInfoException` if more than one certificate is returned.

        
.. method:: connectivity()

    Returns a tuple :code:`(core_address, core_port)` with Greengrass Core address and port if only one Core is returned by discover call.
    Raises :code:`GreengrassDiscoveryInfoException` if more than one Core is returned.        

        
================
Helper Functions
================

.. function:: discover(endpoint, thingname, clicert, pkey, cacert=None)

        :param endpoint: AWS server where to retrieve Greengrass core info
        :param thingname: AWS IoT Core or AWS Greengrass Device name
        :param clicert: client certificate
        :param pkey: client private key

    Discover info about own group Greengrass Core.
    Returns a :class:`DiscoveryInfo` object.

    
