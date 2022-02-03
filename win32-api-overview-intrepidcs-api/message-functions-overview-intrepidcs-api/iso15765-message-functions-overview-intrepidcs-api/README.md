# ISO15765 Message Functions Overview - intrepidcs API

| Name                   | Description                                                                 |
| ---------------------- | --------------------------------------------------------------------------- |
| ISO15765EnableNetworks | Enables ISO15765 functions. Must be called before Tx and RX functions.      |
| ISO15765TxMessage      | Sends a ISO15765 message on CAN.                                            |
| ISO15765RxMessage      | Looks for specified frames and responds with specified flow control on CAN. |
