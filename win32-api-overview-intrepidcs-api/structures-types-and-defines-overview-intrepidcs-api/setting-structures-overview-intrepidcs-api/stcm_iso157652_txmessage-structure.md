# stCM\_ISO157652\_TxMessage Structure

This structure is used by icsneoISO15765\_TransmitMessage

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
typedef struct __declspec(align(2)) _stCM_ISO157652_TxMessage
{
    unsigned short vs_netid; 
    unsigned char padding; 
    unsigned char reserved2;
    unsigned int id; 
    unsigned int fc_id; 
    unsigned int fc_id_mask; 
    unsigned char stMin;
    unsigned char blockSize;
    unsigned char flowControlExtendedAddress; 
    unsigned char extendedAddress; 

    unsigned short fs_timeout; 
    unsigned short fs_wait; 
   
    unsigned char data[4*1024]; 
    unsigned int num_bytes;
    union
    { 
        struct
        {
            unsigned id_29_bit_enable:1; 
            unsigned fc_id_29_bit_enable:1; 
            unsigned ext_address_enable:1; 
            unsigned fc_ext_address_enable:1; 
            unsigned overrideSTmin:1;
            unsigned overrideBlockSize:1;
            unsigned paddingEnable:1;
            unsigned iscanFD : 1;
            unsigned isBRSEnabled : 1;        };
    unsigned short flags;
};

```
{% endtab %}

{% tab title="Visual Basic .NET Declare 1" %}
```vbnet
<StructLayout(LayoutKind.Sequential, Pack:=2)> Public Structure stCM_ISO157652_TxMessage
    Dim vs_netid As UInt16
    Dim padding As Byte
    Dim reserved2 As Byte
    Dim id As UInt32
    Dim fc_id As UInt32
    Dim fc_id_mask As UInt32
    Dim stMin As Byte
    Dim blockSize As Byte
    Dim flowControlExtendedAddress As Byte 
    Dim extendedAddress As Byte
    '//flow control timeouts
    Dim fs_timeout As UInt16
    Dim fs_wait As UInt16
    '//******************************************************************************************************************
    <VBFixedArray(4095), System.Runtime.InteropServices.MarshalAs(System.Runtime.InteropServices.UnmanagedType.ByValArray, SizeConst:=4095)> Public data() As Byte
    '// call: stCM_ISO157652_TxMessage.data = New Byte(4096) {}
    '//******************************************************************************************************************
    Dim num_bytes As UInt32
    Dim flags As UInt16
End Structure
```
{% endtab %}

{% tab title="Visual Basic .NET Declare 2" %}
```vbnet
Enum stCM_ISO157652_TxMessage_Flags
    id_29_bit_enable = 1 
    fc_id_29_bit_enable = 2 
    ext_address_enable = 4 
    fc_ext_address_enable = 8 
    overrideSTmin = 16 
    overrideBlockSize = 32 
    paddingEnable = 64 
    iscanFD = 128 
    isBRSEnabled= 256
End Enum
```
{% endtab %}

{% tab title="C# Declare 1" %}
```csharp
[StructLayout(LayoutKind.Sequential, Pack = 2)]
public struct {
    public UInt16 vs_netid;
    public byte padding;
    public bytete reserved2;
    public id;
    public UInt32 fc_id; 
    public UInt3232
    public bytete
    public byte blockSize;
    public bytete
    public bytete
    public UInt16 fs_timeout;
    public UInt16 fs_wait; 
    //******************************************************************************************************************
    [MarshalAs(>(UnmanagedType.ByValArray,SizeConst=4095)] public byte[] data;
    // call: stCM_ISO157652_TxMessage.data = new byte(4096)
    //******************************************************************************************************************
    public num_bytes;
    public UInt16 flags;
}
```
{% endtab %}

{% tab title="C# Declare 2" %}
```csharp
public enum stCM_ISO157652_TxMessage_Flags : int
{
    id_29_bit_enable = 1,
    fc_id_29_bit_enable = 2, 
    ext_address_enable = 4, 
    fc_ext_address_enable = 8, 
    overrideSTmin = 16, 
    overrideBlockSize = 32, 
    paddingEnable = 64, 
    iscanFD = 128,
    isBRSEnabled= 256,
}

```
{% endtab %}
{% endtabs %}
