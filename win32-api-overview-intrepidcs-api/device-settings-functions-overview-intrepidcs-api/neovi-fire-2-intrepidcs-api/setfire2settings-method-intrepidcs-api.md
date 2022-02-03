# SetFire2Settings Method - intrepidcs API

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoSetFire2Settings(void * hObject, SFIRE2Settings *pSettings, int iNumBytes, int bSaveToEEPROM);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoSetFire2SettingsLib “icsneo40.dll” (ByVal hObject As IntPtr, ByRef pSettings As SFIRE2Settings, ByVal iNumBytes As Int32, ByVal bSaveToEEPROM As Int32) As Int32
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern Int32 icsneoSetFire2Settings(IntPtr hObject, ref SFIRE2Settings pSettings, Int32 iNumBytes, Int32 bSaveToEEPROM);
```
{% endtab %}
{% endtabs %}

**Parameters**

hObject

\[in] Specifies the driver object created by OpenNeoDevice.

pSettings

\[in] The address of an allocated SFIRE2Settings structure.

iNumBytes

\[in] This value is always the size, in bytes, of the SFIRE2Settings structure.

bSaveToEEPROM

\[in] If set to 0, the settings changes will revert to the values stored in EEPROM when the neoVI FIRE 2 is power-cycled. If set to 1, the values will overwrite the EEPROM settings and become persistent across power-cycles of the neoVI FIRE 2.

**Return Values**

Returns 1 if successful, 0 if an error occurred. GetLastAPIError must be called to obtain the specific error. The errors that can be generated by this function are:

NEOVI\_ERROR\_DLL\_NEOVI\_NO\_RESPONSE = 75

**Remarks**

Before using this function, the SFIRE2Settings structure must be initialized with the current neoVI settings using GetFIRE2Settings.

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```
SFIRE2Settings Fire2ReadSettings;
int iNumberOfBytes;
int iResult;

//################################
//Fire2ReadSettings struct is read
//and changed as needed before
//Setting the new values
//################################

iNumberOfBytes=sizeof(Fire2ReadSettings);
iResult = icsneoSetFIRE2Settings(m_hObject, &Fire2ReadSettings , iNumberOfBytes, 1);
if(iResult == 0)
{
    MessageBox::Show("Problem Sending FIRE2 configuration");
    return;
}
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
SFIRE2Settings = new Fire2ReadSettings();
int iNumberOfBytes;
int iResult;

//################################
//Fire2ReadSettings struct is read
//and changed as needed before
//Setting the new values
//################################

iNumberOfBytes = System.Runtime.InteropServices.Marshal.SizeOf(Fire2ReadSettings);
iResult = icsNeoDll.icsneoSetFIRE2Settings(m_hObject, ref Fire2ReadSettings , iNumberOfBytes, 1);

if(iResult == 0)
{
    MessageBox.Show("Problem Sending FIRE2 configuration");
    return;
}
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
Dim Fire2ReadSettings As SFIRE2Settings
Dim iNumberOfBytes As Integer
Dim iResult As Integer

'//################################
'//Fire2ReadSettings struct is read
'//and changed as needed before
'//Setting the new values
'//################################

iNumberOfBytes = System.Runtime.InteropServices.Marshal.SizeOf(Fire2ReadSettings)
iResult = icsneoSetFIRE2Settings(m_hObject, Fire2ReadSettings , iNumberOfBytes, 1)

If iResult = 0 Then
    MsgBox("Problem Sending FIRE2 configuration")
    Exit Sub
End If
```
{% endtab %}
{% endtabs %}