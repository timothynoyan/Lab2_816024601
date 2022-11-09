## Part 1

The project "GPIO" from [Lab 1](https://github.com/timothynoyan/Lab1_Q2_816024601) was used to identify the following files.

### /project/sdkconfig

Each new project contains the sdkconfig file, an application-specific configuration file. The settings for connecting with and flashing the ESP8266 are specified in this file. If caution is not exercised, it might adversely affect the flashing and serial monitoring processes.

### /project/build/include/sdkconfig.h

When the project is built, the sdkconfig.h header file is created. The settings from the sdkconfig file are translated into a header file. Hence, if errors are made in the sdkconfig file, it would affect this file as well.
 
### /sdk/components/freertos/port/esp8266/include/freertos/FreeRTOSConfig.h

The FreeRTOS kernel defaults are specified in the FreeRTOSConfig.h file. The features and functions of the RTOS that are used in our projects are managed by this file. FreeRTOS-specific features and functions can be enabled or disabled by making changes to this file.


## Part 2

The **vTaskGetRunTimeStats()** API function may be used to obtain task performance statistics.

FreeRTOS can track the amount of processing time used by each task. The FreeRTOS runtime statistics function may then be used to display this data. However, this option is not activated by default. To enable this feature, the following are required:
* configGENERATE_RUN_TIME_STATS
* portCONFIGURE_TIMER_FOR_RUN_TIME_STATS()
* portGET_RUN_TIME_COUNTER_VALUE()

**configGENERATE_RUN_TIME_STATS** - Must be set to 1 to enable the vTaskGetRunTimeStats() function.

**portCONFIGURE_TIMER_FOR_RUN_TIME_STATS() vSetupTimerForRunTimeStats()** - The vSetupTimerForRunTimeStats() function is a user-defined function that determines run-time statistics.

**portGET_RUN_TIME_COUNTER_VALUE()** - This is required to get the current time value.
