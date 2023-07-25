API Reference Guide
===================

.. raw:: html

   <hr>

The following reference guide outlines the API of `EZBotball`_.

Locomotion
=============

.. raw:: html

   <hr>

The most optimal methods for moving robots, using the Gyroscope and advanced mathematic methods.

example_drive(*speed*, *time*)
---------------------------

Parameters
^^^^^^^^^^
* **speed** (`int`_) - The speed of the motors. Accepts values 0-100.
* **time** (`int`_) - The amount of time for the robot to drive forward in seconds.

KIPR Functions
^^^^^^^^^^^^^^
* `mav`_ (*motor*, *velocity*)

Servos
=============

.. raw:: html

   <hr>

example_servo(*speed*, *time*)
---------------------------

Parameters
^^^^^^^^^^
* **speed** (`int`_) - The speed of the motors. Accepts values 0-100.
* **time** (`int`_) - The amount of time for the robot to drive forward in seconds.

KIPR Functions
^^^^^^^^^^^^^^
* `mav`_ (*motor*, *velocity*)

Sensors
=============

.. raw:: html

   <hr>

example_sensor(*speed*, *time*)
---------------------------

Parameters
^^^^^^^^^^
* **speed** (`int`_) - The speed of the motors. Accepts values 0-100.
* **time** (`int`_) - The amount of time for the robot to drive forward in seconds.

KIPR Functions
^^^^^^^^^^^^^^
* `mav`_ (*motor*, *velocity*)

Helpers
=============

example_helper(*speed*, *time*)
---------------------------

Parameters
^^^^^^^^^^
* **speed** (`int`_) - The speed of the motors. Accepts values 0-100.
* **time** (`int`_) - The amount of time for the robot to drive forward in seconds.

KIPR Functions
^^^^^^^^^^^^^^
* `mav`_ (*motor*, *velocity*)

.. raw:: html

   <hr>

.. _EZBotball: https://github.com/EZBotball
.. _int: https://devdocs.io/c/language/types
.. _mav: https://www.kipr.org/doc/group__motor.html#gabd36f01986c363f70d86c7a768ae1348
