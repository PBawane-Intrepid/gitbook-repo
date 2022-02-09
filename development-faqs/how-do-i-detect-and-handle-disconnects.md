# How do I detect and handle disconnects?

If the neoVI is removed from the computer or stops responding, most API calls will generate a disconnect error. If you receive a return value from an API call that indicates an error occurred, you must call the GetLastAPIError method. If the error is `NEOVI_ERROR_DLL_NEOVI_NO_RESPONSE` then the neoVI has either been unplugged or is not responding.

To recover from this condition follow these steps:

* Plug the neoVI back in, or in the case of the neoVI not responding, remove and then plug back in.
* Call the ClosePort method.
* Call the OpenNeoDevice method using the same parameters are before.

The following API functions will generate the NEOVI\_ERROR\_DLL\_NEOVI\_NO\_RESPONSE error:

| Function                          |
| --------------------------------- |
| GetMessages                       |
| TxMessages                        |
| WaitForRxMessagesWithTimeOut      |
| GetTimeStampForMsg                |
| EnableNetworkCom                  |
| GetConfiguration                  |
| SendConfiguration                 |
| GetFireSettings                   |
| SetFireSettings                   |
| GetVCAN3Settings                  |
| SetVCAN3Settings                  |
| SetBitRate                        |
| GetDeviceParameters               |
| SetDeviceParameters               |
| ScriptLoad                        |
| ScriptStart                       |
| ScriptStop                        |
| ScriptClear                       |
| ScriptStartFBlock                 |
| ScriptStopFBlock                  |
| ScriptGetFBlockStatus             |
| ScriptGetScriptStatus             |
| ScriptReadAppSignal               |
| ScriptWriteAppSignal              |
| ScriptReadRxMessage               |
| ScriptReadTxMessage               |
| ScriptWriteRxMessage              |
| ScriptWriteTxMessage              |
| ScriptReadISO15765\_2\_TxMessage  |
| ScriptWriteISO15765\_2\_TxMessage |
