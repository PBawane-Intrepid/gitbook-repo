# Message Functions Overview - intrepidcs API

| Name                         | Description                                                                                |
| ---------------------------- | ------------------------------------------------------------------------------------------ |
| GetMessages                  | Reads messages from the neoVI device.                                                      |
| TxMessages                   | Transmits messages to vehicle networks using a neoVI device.                               |
| TxMessagesEx                 | Transmits messages to vehicle networks using a neoVI device. Used with CAN FD and Ethernet |
| WaitForRxMessagesWithTimeOut | Waits a specified amount of time in milliseconds for a received message                    |
| GetTimeStampForMsg           | Calculates and returns the timestamp for a message                                         |
| ISO15765 Functions           | Functions for ISO15765 transactions.                                                       |
| Transmitting Long Messages   | Example for sending longer (<12 bytes) ISO9141/KW2K Messages                               |
