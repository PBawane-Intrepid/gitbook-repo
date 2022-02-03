# SetFDBitRate Method - intrepidcs API

This method sets bit rates for networks on neoVI devices

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoSetFDBitRate(void * hObject, int iBitRate, int iNetworkID);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoSetFDBitRate Lib “icsneo40.dll” (ByVal hObject As IntPtr, ByVal BitRate As Int32, ByVal NetworkID As Int32) As Int32
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern Int32 icsneoSetFDBitRate(IntPtr hObject, Int32 BitRate, Int32 NetworkID);
```
{% endtab %}
{% endtabs %}

**Parameters**

hObject

\[in] Specifies the driver object created by OpenNeoDevice.

iBitRate

\[in] Specifies bit rate setting. Valid values depend on the network specified.

> For the networks HSCAN, MSCAN, HSCAN2, HSCAN3, HSCAN4, HSCAN5, HSCAN6, and HSCAN7 valid bit rates are 1000000, 2000000, 4000000, 5000000, 8000000,and 10000000

iNetworkID

\[in] Specifies the network. The valid values are:

> NETID\_HSCAN, NETID\_MSCAN, NETID\_HSCAN2, NETID\_HSCAN3, NETID\_HSCAN4, NETID\_HSCAN5, NETID\_HSCAN6, and NETID\_HSCAN7

These values are defined in the icsnVC40.h file

**Return Values**

1 if the function succeeded. 0 if it failed for any reason. GetLastAPIError must be called to obtain the specific error. The errors that can be generated by this function are:

NEOVI\_ERROR\_DLL\_INVALID\_NETID = 8

NEOVI\_ERROR\_DLL\_NEOVI\_NO\_RESPONSE = 75

NEOVI\_ERROR\_DLL\_RED\_INVALID\_BAUD\_SPECIFIED = 122

NEOVI\_ERROR\_DLL\_SEND\_DEVICE\_CONFIG\_ERROR = 229

NEOVI\_ERROR\_DLL\_GET\_DEVICE\_CONFIG\_ERROR = 230

NEOVI\_ERROR\_DLL\_UNKNOWN\_NEOVI\_TYPE = 231

**Remarks**

The specified network must exist on the connected neoVI device.

### Examples

{% tabs %}
{% tab title="C/C++ Example:" %}
```cpp
int iRetVal;

iRetVal = icsneoSetFDBitrate(hObject, 5000000, NETID_HSCAN);
if(iRetVal == 0)
{
    printf("\nFailed to set the bit rate");
}
else
{
    printf("\nSuccessfully set the bit rate");
}
```
{% endtab %}

{% tab title="C# Example:" %}
```csharp
int iResult;

//Set the bit rate
iResult = icsNeoDll.icsneoSetFDBitRate(m_hObject, 5000000, NETID_HSCAN);
if (iResult == 0)
{
    MessageBox.Show("Problem setting bit rate");
}
```
{% endtab %}

{% tab title="Visual Basic .NET Example:" %}
```vbnet
Dim iResult As Integer
'//Set the bit rate
iResult = icsneoSetFDBitRate(m_hObject, 5000000, NETID_HSCAN)
If (iResult = 0) Then MsgBox("Problem setting bit rate")
```
{% endtab %}
{% endtabs %}