Introduction
============

CircuitPython helper library for the MPU6886 6-DoF Accelerometer and Gyroscope

.. image:: https://img.shields.io/discord/327254708534116352.svg
    :target: https://adafru.it/discord
    :alt: Discord


.. image:: https://github.com/jins-tkomoda/CircuitPython_MPU6886/workflows/Build%20CI/badge.svg
    :target: https://github.com/jins-tkomoda/CircuitPython_MPU6886/actions
    :alt: Build Status


.. image:: https://img.shields.io/badge/code%20style-black-000000.svg
    :target: https://github.com/psf/black
    :alt: Code Style: Black

CircuitPython helper library for the MPU6886 6-DoF Accelerometer and Gyroscope


Dependencies
=============
This driver depends on:

* `Adafruit CircuitPython <https://github.com/adafruit/circuitpython>`_

Please ensure all dependencies are available on the CircuitPython filesystem.
This is easily achieved by downloading
`the Adafruit library and driver bundle <https://circuitpython.org/libraries>`_
or individual libraries can be installed using
`circup <https://github.com/adafruit/circup>`_.

Installing from PyPI
=====================
.. note:: This library is not available on PyPI yet. Install documentation is included
   as a standard element. Stay tuned for PyPI availability!

.. todo:: Remove the above note if PyPI version is/will be available at time of release.

On supported GNU/Linux systems like the Raspberry Pi, you can install the driver locally `from
PyPI <https://pypi.org/project/circuitpython-mpu6886/>`_.
To install for current user:

.. code-block:: shell

    pip3 install circuitpython-mpu6886

To install system-wide (this may be required in some cases):

.. code-block:: shell

    sudo pip3 install circuitpython-mpu6886

To install in a virtual environment in your current project:

.. code-block:: shell

    mkdir project-name && cd project-name
    python3 -m venv .venv
    source .env/bin/activate
    pip3 install circuitpython-mpu6886

Installing to a Connected CircuitPython Device with Circup
==========================================================

Make sure that you have ``circup`` installed in your Python environment.
Install it with the following command if necessary:

.. code-block:: shell

    pip3 install circup

With ``circup`` installed and your CircuitPython device connected use the
following command to install:

.. code-block:: shell

    circup install mpu6886

Or the following command to update an existing version:

.. code-block:: shell

    circup update

Usage Example
=============

.. code-block:: python3
    
    import time
    import board
    import mpu6886

    i2c = board.I2C()  # uses board.SCL and board.SDA
    mpu = mpu6886.MPU6886(i2c)

    while True:
        print("Acceleration: X:%.2f, Y: %.2f, Z: %.2f m/s^2"%(mpu.acceleration))
        print("Gyro X:%.2f, Y: %.2f, Z: %.2f degrees/s"%(mpu.gyro))
        print("Temperature: %.2f C"%mpu.temperature)
        print("")
        time.sleep(1)

Documentation
=============
API documentation for this library can be found on `Read the Docs <https://circuitpython-mpu6886.readthedocs.io/>`_.

For information on building library documentation, please check out
`this guide <https://learn.adafruit.com/creating-and-sharing-a-circuitpython-library/sharing-our-docs-on-readthedocs#sphinx-5-1>`_.

Contributing
============

Contributions are welcome! Please read our `Code of Conduct
<https://github.com/jins-tkomoda/CircuitPython_MPU6886/blob/HEAD/CODE_OF_CONDUCT.md>`_
before contributing to help this project stay welcoming.