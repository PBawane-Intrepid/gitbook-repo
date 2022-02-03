---
cover: ../.gitbook/assets/new-cover-image.png
coverY: 0
---

# WIN32 API Overview - IntrepidCS API

**Basic Operations**

| Name                                                                                            | Description                                                                 |
| ----------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| [FindDevices](basic-functions-overview-intrepidcs-api/finddevices-method.md)                    | Used to locate connected neoVI and ValueCAN devices.                        |
| [OpenNeoDevice](basic-functions-overview-intrepidcs-api/openneodevice-method-intrepidcs-api.md) | Used to open a communication link with a specific neoVI or ValueCAN device. |
| [ClosePort](basic-functions-overview-intrepidcs-api/closeport-method-intrepidcs-api.md)         | Closes the communication link with the neoVI device.                        |
| [FreeObject](basic-functions-overview-intrepidcs-api/freeobject-method-intrepidcs-api.md)       | Releases system resources used by the neoVI device.                         |

**Message Functions**

| Name                         | Description                                                                                                                |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| GetMessages                  | Reads messages from the neoVI or ValueCAN device.                                                                          |
| TxMessages                   | Transmits messages to vehicle networks using a neoVI or ValueCAN device.                                                   |
| TxMessagesEx                 | Transmits messages longer than 8 bytes to vehicle networks using a neoVI or ValueCAN device. Used with Ethernet and CAN FD |
| WaitForRxMessagesWithTimeOut | Waits a specified amount of time in milliseconds for a received message                                                    |
| GetTimeStampForMSG           | Calculates the timestamp for a message given the handle to the device and a Message Structure                              |
| ISO15765EnableNetworks       | Enables ISO15765 for the selective CAN/CANFD network                                                                       |
| ISO15765TxMessage            | Configures an outgoing ISO15765 transaction                                                                                |
| ICS15765RxMessage            | Configures the hardware to listen for a ISO15765 transaction                                                               |
| Transmitting Long Messages   | In formation on sending longer frames on ISO9171 and Keyword 2000 networks                                                 |

**Device Settings Functions**

| Name                         | Description                                                                 |
| ---------------------------- | --------------------------------------------------------------------------- |
| GetConfiguration             | Reads the configuration bytes for a neoVI Blue or ValueCAN device           |
| SendConfiguration            | Sends configuration bytes to a neoVI Blue or ValueCAN device                |
| GetFireSettings              | Gets device and network parameters for a neoVI Fire device                  |
| SetFireSettings              | Sets device and network parameters for a neoVI Fire device                  |
| GetFIRE2Settings             | Gets device and network parameters for a neoVI Fire 2 device                |
| SetFIRE2Settings             | Sets device and network parameters for a neoVI Fire 2 device                |
| GetVCAN3Settings             | Gets device and network parameters for a ValueCAN3 device                   |
| SetVCAN3Settings             | Sets device and network parameters for a ValueCAN3 device                   |
| GetVCAN412Settings           | Gets device and network parameters for a ValueCAN4-1 and ValueCAN4-2 device |
| SetVCAN412Settings           | Sets device and network parameters for a ValueCAN4-1 and ValueCAN4-2 device |
| GetVCANRFSettings            | Gets device and network parameters for a ValueCAN RF device                 |
| SetVCANRFSettings            | Sets device and network parameters for a ValueCAN RF device                 |
| GetRADGalaxySettings         | Gets device and network parameters for a RAD Galaxy device                  |
| SetRADGalaxySettings         | Sets device and network parameters for a RAD Galaxy device                  |
| SetBitRate                   | Set the baud or bit rate for a specific neoVI network                       |
| GetHWFirmwareInfo            | Gets the firmware version of a neoVI device                                 |
| GetDLLFirmwareInfo           | Gets the firmware version stored in the DLL API                             |
| ForceFirmwareUpdate          | Forces the firmware to updated on a neoVI device                            |
| GetDeviceParameters          | Gets individual parameters for a neoVI device                               |
| SetDeviceParameters          | Sets individual parameters for a neoVI device                               |
| SetReflashDisplayCallbacks   | Sets callback function pointers for flashing a neoVI                        |
| ClearReflashDisplayCallbacks | Clears callback function pointers for flashing a neoVI                      |
| GetRTC                       | Gets the current real-time clock value from a connect neoVI device          |
| SetRTC                       | Sets the current real-time clock value in a connected neoVI device          |

**Error Functions**

| Name             | Description                                                 |
| ---------------- | ----------------------------------------------------------- |
| GetLastAPIError  | Returns the error generated by the last intrepidcs API call |
| GetErrorMessages | Returns the intrepidcs API error message queue              |
| GetErrorInfo     | Returns a text description of an intrepidcs API error       |

**General Utility Functions**

| Name                     | Description                                            |
| ------------------------ | ------------------------------------------------------ |
| ValidateHObject          | Used to determine if an hObject reference is valid     |
| GetDLLVersion            | Returns DLL version information                        |
| StartSockServer          | Starts the TCP/IP socket server at a specified port.   |
| StopSockServer           | Stops the TCP/IP socket server                         |
| GetPerformanceParameters | Returns information on performance of dll and hardware |

#### CoreMini Functions

| Function                     | Description                                                                                         |
| ---------------------------- | --------------------------------------------------------------------------------------------------- |
| ScriptStart                  | Starts execution of a script that has been downloaded to a neoVI device                             |
| ScriptStop                   | Stops execution of a script running on a neoVI device                                               |
| ScriptLoad                   | Downloads a script to a connected neoVI device into a specified location                            |
| ScriptClear                  | Clears a script from a specific location on a neoVI device                                          |
| ScriptStartFBlock            | Starts a function block within a script on a neoVI device                                           |
| ScriptGetFBlockStatus        | Returns the run status of a function block within a script on a neoVI device                        |
| ScriptStopFBlock             | Stops the execution of a function block within a script on a neoVI device                           |
| ScriptGetScriptStatus        | Stops the execution of a function block within a script on a neoVI device                           |
| ScriptReadAppSignal          | Read an application signal from a script running on a neoVI device                                  |
| ScriptWriteAppSignal         | Set the value of an application signal in a script running on a neoVI device                        |
| ScriptReadISO15765TxMessage  | Read parameters of an ISO15765-2 long transmit message in a script on a neoVI device                |
| ScriptWriteISO15765TxMessage | Change the parameters for an ISO15765-2 long transmit message defined in a script on a neoVI device |

#### Deprecated Functions

| Name                 | Description                                                                       |
| -------------------- | --------------------------------------------------------------------------------- |
| OpenPortEx           | Use OpenNeoDevice instead                                                         |
| OpenPort             | Use OpenNeoDevice instead                                                         |
| EnableNetworkCom     | It is no longer necessary to call this before and after calling SendConfiguration |
| FindAllUSBDevices    | No longer supported. It is present in the API but will always return 0            |
| ScriptReadRxMessage  | Reads parameters for a receive message defined in a script on a neoVI device      |
| ScriptReadTxMessage  | Reads parameters for a transmit message defined within a script on a neoVI device |
| ScriptWriteRxMessage | Alter a receive message defined within script on a neoVI device                   |
| ScriptWriteTxMessage | Alter a transmit message defined within a script on a neoVI device                |
