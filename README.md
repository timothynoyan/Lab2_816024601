## Part 1

The project "GPIO" from Lab 1 was used to identify the following files.

### /project/sdkconfig

Each new project contains the sdkconfig file, an application-specific configuration file. The settings for connecting with and flashing the ESP8266 are specified in this file. If caution is not exercised, it might adversely affect the flashing and serial monitoring processes.

### /project/build/include/sdkconfig.h

When the project is built, the sdkconfig.h header file is created. The settings from the sdkconfig file are translated into a header file. Hence, if errors are made in the sdkconfig file, it would affect this file as well.
 
