# How do I open more than one channel on a single piece of hardware? - intrepidcs API

When calling OpenNeoDevice or OpenPortEx to connect to the device, all the enabled channels on the device are active. Nothing special needs to be done "open" another channel. Calling GetMessages will get messages on all enabled channels. Looking at the NetworkID in the message structure for that message, the channel the message occurred on can be determined. When transmitting a message using TxMessage, the third parameter is the Network ID to send the message out on.
