Helpers
=============

Helper functions.

``viprint(val)``
---------------------------

a simple debugging function used for easily printing integer values

Parameters
^^^^^^^^^^
   * **val** (`int`_) - the value to be printed, any valid integer

.. raw:: html

   <hr>

``vfprint(val)``
---------------------------

a simple debugging function used for easily printing float values

Parameters
^^^^^^^^^^
   * **val** (`int`_) - the value to be printed, any valid float

.. raw:: html
   <hr>

``clear_wheels()``
---------------------------

clears the motor position for both the left and right wheels of the robot as determined by
the left and right wheel defines


KIPR Functions
^^^^^^^^^^^^^^
    * `cmpc`_(*port*)

.. raw:: html
   <hr>

``set_accel_window(distance)``
---------------------------

used the set the accel and deccel of locomotion functions

Parameters
^^^^^^^^^^
   * **distance** (`float`_) - the distance of the acceleration and deceleration in cm

.. raw:: html

   <hr>

``analog_avg(port,loops)``
---------------------------
basic function used to average the analog sensors for a certain amount of loops
there is a 5 millisecond delay in between that data collection

Parameters
^^^^^^^^^^
   * **port** (`int`_) - the port of the analog sensor
   * **loops** (`int`_) - how many times that data is collected for the average

.. raw:: html

   <hr>

``calculate_location_change(right_movement, left_movement, theta)``
---------------------------
this function returns a Struct of type position holding the change in x, y, and theta based on
the given input. The math does not account for the perfect curve of the driven distance, and 
instead uses much simpler triangular math becuase it is supposed to be sampled fast inside of a loop. 
But because it can sample so much faster with easier equations, under light experimentation the simpler
math has shown better results than the more complicated and correct math

Parameters
^^^^^^^^^^
   * **right_movement** (`double`_) - the distance the right wheel has travelled since last sample
   * **left_movement** (`double`_) - the distance the left wheel has travelled since last sample
   * **theta** (`double`_) - the overall angle of the robot since the start of the loop, **this is unlike the previous two parameters that only ask for change in movement that loop**

.. raw:: html

   <hr>

``calculate_speed_ramp(final_dist, current_dist)``
---------------------------
returns a float value from 0 to 1 that can be multiplied to a speed. Used internally in locomotion functions
to smake the accel and decel curve

Parameters
^^^^^^^^^^
   * **final_dist** (`float`_) - the total distance that needs to be travelled in cm
   * **current_dist** (`float`_) - the current distance travelled in cm

.. raw:: html

   <hr>

``in_range(current, desired, spread)``
---------------------------
a simple calculation function that returns 1 if a value is in range of a desired number and 0 if it is not

Parameters
^^^^^^^^^^
   * **current** (`float`_) - the current value
   * **desired** (`float`_) - tthe desired value
   * **spread** (`float`_) - the spread both left and right of the desired value for which to look for the current value in

.. raw:: html

   <hr>


.. _int: https://devdocs.io/c/language/types
.. _float: https://devdocs.io/c/language/types
.. _double: https://devdocs.io/c/language/types 
.. _cmpc: https://files.kipr.org/wallaby/wallaby_doc/group__motor.html#ga3f000f325222eb01b69844290a654795
.. _mav: https://www.kipr.org/doc/group__motor.html#gabd36f01986c363f70d86c7a768ae1348
