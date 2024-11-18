# STM32WBA55_BLE_HeartRate_Client

* The STM32WBA55_BLE_HeartRate_Client is based on the BLE_P2PClient application from STM32CubeWBA V1.4.1.
* This application is an example of a BLE Client for the BLE_HeartRate project from STM32CubeWBA.
* This project has the following button functionality:
    * SW1 (Disconnected) : Start BLE scanning and automatic connection.
    * SW1 (Connected)    : Send a BLE write to the Heart Rate Control Point characteristic.
    * SW2 (Disconnected) : Clear security database (BLE bonding information).
    * SW2 (Connected)    : Send a BLE read request to the Body Sensor Location characteristic.
    * SW3 (Disconnected) : No functionality.
    * SW3 (Connected)    : Toggle the Heart Rate Measurement characteristic notifications.
* Check the BLE_HeartRate [WIKI page](https://wiki.st.com/stm32mcu/wiki/Connectivity:STM32WBA_HeartRate) for information on the server application from STM32CubeWBA.

## Hardware Needed

  * Two [NUCLEO-WBA55CG](https://www.st.com/en/evaluation-tools/nucleo-wba55cg.html)
    * One for STM32WBA55_BLE_HeartRate_Client
    * One for [BLE_HeartRate](https://github.com/STMicroelectronics/STM32CubeWBA/tree/main/Projects/NUCLEO-WBA55CG/Applications/BLE/BLE_HeartRate) from STM32CubeWBA

## Software Needed

  * Prebuilt firmware image: STM32WBA55_BLE_HeartRate_Client.hex (STM32WBA55_BLE_HeartRate_Client\Binary)

  * [STM32CubeWBA](https://www.st.com/en/embedded-software/stm32cubewba.html)

  * [STM32CubeProgrammer](https://www.st.com/en/development-tools/stm32cubeprog.html)

  * IDE (Optional)

    * [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html)

    * [IAR EWARM](https://www.iar.com/products/architectures/arm/iar-embedded-workbench-for-arm/)

    * [Keil MDK-ARM](https://developer.arm.com/Tools%20and%20Software/Keil%20MDK)

  * [Tera Term](https://teratermproject.github.io/index-en.html) (Optional)

## User's Guide

1) Flash the NUCLEO-WBA55 with the application using one of the following methods:

    a) Flash the prebuilt firmware image with STM32CubeProgrammer.

    ![RM_IMAGE_0](Utilities/Media/RM_IMAGE_0.png)

    b) Build and debug the application with an IDE.

    ![RM_IMAGE_1](Utilities/Media/RM_IMAGE_1.png)

2) View the debug log output using Tera Term, you may need to press the reset button to view the inital logs (optional).

    a) Left: BLE Heart Rate Client

    b) Right: BLE Heart Rate Server 
    
    > Note: CFG_LOG_SUPPORTED, CFG_LPM_LEVEL, & CFG_LPM_STDBY_SUPPORTED in app_conf.h will need to be modified to see the logs for the BLE_HeartRate example.

![RM_IMAGE_2](Utilities/Media/RM_IMAGE_2.png)

3) Press SW1 on the STM32WBA55_BLE_HeartRate_Client device to start scanning and automatic connection.

![RM_IMAGE_3](Utilities/Media/RM_IMAGE_3.png)

4) The STM32WBA55_BLE_HeartRate_Client will perform service, characteristic, and descriptor discovery upon connection.

![RM_IMAGE_4](Utilities/Media/RM_IMAGE_4.png)

5) The Heart Rate Measurement notifications will be enabled upon connection as well. 

![RM_IMAGE_5](Utilities/Media/RM_IMAGE_5.png)

6) Press SW3 on the STM32WBA55_BLE_HeartRate_Client device to toggle the Heart Rate Measurement notifications.

![RM_IMAGE_6](Utilities/Media/RM_IMAGE_6.png)

7) Press SW1 on the STM32WBA55_BLE_HeartRate_Client device to send a BLE write to the Heart Rate Control Point characteristic.

![RM_IMAGE_7](Utilities/Media/RM_IMAGE_7.png)

8) Press SW2 on the STM32WBA55_BLE_HeartRate_Client device to send a BLE read request to the Body Sensor Location characteristic.

![RM_IMAGE_8](Utilities/Media/RM_IMAGE_8.png)

## Troubleshooting

**Caution** : Issues and the pull-requests are **not supported** to submit problems or suggestions related to the software delivered in this repository. The STM32WBA55_BLE_HeartRate_Client example is being delivered as-is, and not necessarily supported by ST.

**For any other question** related to the product, the hardware performance or characteristics, the tools, the environment, you can submit it to the **ST Community** on the STM32 MCUs related [page](https://community.st.com/s/topic/0TO0X000000BSqSWAW/stm32-mcus).