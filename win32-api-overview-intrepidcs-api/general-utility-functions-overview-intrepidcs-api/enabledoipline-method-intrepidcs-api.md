# EnableDOIPLine Method - intrepidcs API

This method enables or disables the Ethernet activation line on supported hardware devices.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
int _stdcall icsneoEnableDOIPLine(void* hObject, bool bActivate);
```
{% endtab %}

{% tab title="Visual Basic .NET Declare" %}
```vbnet
Public Declare Function icsneoEnableDOIPLine Lib “icsneo40.dll” (ByVal hObject As IntPtr, ByVal bActivate As Boolean) As Int32
```
{% endtab %}

{% tab title="C# Declare" %}
```csharp
[DllImport(“icsneo40.dll”)] public static extern Int32 icsneoEnableDOIPLine(IntPtr hObject, bool bActivate);
```
{% endtab %}
{% endtabs %}

**Parameters**

hObject

\[in] Handle \[in] Which specifies the driver object created by OpenNeoDevice

bActivate \[in] Sets the state of the Ethernet Activation line.

**Return Values**

This function returns the 1 when successful. 0 if otherwise.

**Remarks**

This function will enable and disable Ethernet Activation line for DoIP applications on applicable hardware devices.

### Examples

{% tabs %}
{% tab title="C/C++ Example" %}
```cpp
icsneoEnableDOIPLine(m_hObject,true);
```
{% endtab %}

{% tab title="Visual Basic .NET Example" %}
```vbnet
Call icsneoEnableDOIPLine (m_hObject, true)
```
{% endtab %}

{% tab title="C# Example" %}
```csharp
icsNeoDll.icsneoEnableDOIPLine(m_hObject,true);
```
{% endtab %}
{% endtabs %}
