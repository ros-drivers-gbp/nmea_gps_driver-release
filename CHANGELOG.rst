^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
Change log for nmea_gps_driver package
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

0.3.2 (2013-07-21)
-------------------
* Moved all new functionaliaty to nmea_navsat_driver and nmea_msgs packages. nmea_gps_driver will be removed in Indigo.

0.3.1 (2013-05-07)
-------------------
* Removed incorrect find_package dependencies

0.3.0 (2013-05-05)
-------------------
* Initial release for Hydro
* Converted to Catkin
* nmea_gps_driver.py is now deprecated and will be removed in I-Turtle. Replacement node is nmea_serial_driver.py .
* Refactored code into NMEA parser, common ROS driver and separate nodes for reading directly from serial or from topic.
* Bugs fixed:

  - nmea_gps_driver crashes when a sentence doesn't have a checksum * character ( http://kforge.ros.org/gpsdrivers/trac/ticket/4 )
  - Add ability for nmea_gps_driver to support reading from string topic ( https://github.com/ros-drivers/nmea_gps_driver/issues/1 ). Use the nmea_topic_driver.py node to get this support.

0.2.0 (2012-03-15)
------------------
* Initial version (released into Fuerte)
* Supports GGA or RMC+GSA sentences to generate sensor_msgs/NavSatFix messages
