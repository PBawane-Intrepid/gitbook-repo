# stAPIFirmwareInfo Structure

This structure continues information regarding the firmware version of a neoVI device.

{% tabs %}
{% tab title="C/C++ Declare" %}
```cpp
struct stAPIFirmwareInfo
{
    int iType;
    // Date and Time (2nd generation neoVI only. See 2nd Generation neoVI Devices)
    int iMainFirmDateDay;
    int iMainFirmDateMonth;
    int iMainFirmDateYear;
    int iMainFirmDateHour;
    int iMainFirmDateMin;
    int iMainFirmDateSecond;
    int iMainFirmChkSum;

    // Version data (3rd generation neoVI only. See 3rd Generation neoVI Devices)
    unsigned char iAppMajor;
    unsigned char iAppMinor;
    unsigned char iManufactureDay;
    unsigned char iManufactureMonth;
    unsigned short iManufactureYear;
    unsigned char iBoardRevMajor;
    unsigned char iBoardRevMinor;
    unsigned char iBootLoaderVersionMajor;
    unsigned char iBootLoaderVersionMinor;
};
```
{% endtab %}

{% tab title="Visual Basic .NET Declares" %}
```vbnet
Public Structure stAPIFirmwareInfo
    Dim iType As Int32
    '// Date and Time (2nd generation neoVI only. See 2nd Generation neoVI Devices)
    Dim iMainFirmDateDay As Int32
    Dim iMainFirmDateMonth As Int32
    Dim iMainFirmDateYear As Int32
    Dim iMainFirmDateHour As Int32
    Dim iMainFirmDateMin As Int32
    Dim iMainFirmDateSecond As Int32
    Dim iMainFirmChkSum As Int32

    '// Version data (3rd generation neoVI only. See 3rd Generation neoVI Devices)
    Dim iAppMajor As Byte
    Dim iAppMinor As Byte
    Dim iManufactureDay As Byte
    Dim iManufactureMonth As Byte
    Dim iManufactureYear As Int16
    Dim iBoardRevMajor As Byte
    Dim iBoardRevMinor As Byte
    Dim iBootLoaderVersionMajor As Byte
    Dim iBootLoaderVersionMinor As Byte
End Structure
```
{% endtab %}

{% tab title="C# Declares" %}
```csharp
[StructLayout(LayoutKind.Sequential)]
public struct stAPIFirmwareInfo
{
    public int iType;
    // Date and Time (2nd generation neoVI only. See 2nd Generation neoVI Devices)
    public int iMainFirmDateDay;
    public int iMainFirmDateMonth;
    public int iMainFirmDateYear;
    public int iMainFirmDateHour;
    public int iMainFirmDateMin;
    public int iMainFirmDateSecond;
    public int iMainFirmChkSum;

    // Version data (3rd generation neoVI only. See 3rd Generation neoVI Devices)
    public unsigned char iAppMajor;
    public unsigned char iAppMinor;
    public unsigned char iManufactureDay;
    public unsigned char iManufactureMonth;
    public unsigned short iManufactureYear;
    public unsigned char iBoardRevMajor;
    public unsigned char iBoardRevMinor;
    public unsigned char iBootLoaderVersionMajor;
    public unsigned char iBootLoaderVersionMinor;
}
```
{% endtab %}
{% endtabs %}

**Remarks**

**Structure Elements**

| Item                                 | Description                                                                                                                                                  |
| ------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| intiType                             | <p>Indicates the generation of hardware:<br>2 = 2nd generation. See 2nd Generation neoVI Devices<br>3 = 3rd generation. See 3rd Generation neoVI Devices</p> |
| intiMainFirmDateDay                  | 1 - 31 firmware day                                                                                                                                          |
| intiMainFirmDateMonth                | 1 - 12 firmware month                                                                                                                                        |
| intiMainFirmDateYear                 | 4 digit year (i.e. 2008) firmware year                                                                                                                       |
| intiMainFirmDateHour                 | 0 - 23 firmware hour                                                                                                                                         |
| intiMainFirmDateMin                  | 0 - 59 firmware minutes                                                                                                                                      |
| intiMainFirmDateSecond               | 0 - 59 firmware seconds                                                                                                                                      |
| intiMainFirmChkSum                   | Firmware checksum                                                                                                                                            |
| unsigned chariAppMajor               | Application major version (3rd generation neoVI only)                                                                                                        |
| unsigned chariAppMinor               | Application minor version (3rd generation neoVI only)                                                                                                        |
| unsigned chariManufactureDay         | 1 - 31 Manufacture day (3rd generation neoVI only)                                                                                                           |
| unsigned chariManufactureMonth       | 1 - 12 Manufacture month (3rd generation neoVI only)                                                                                                         |
| unsigned shortiManufactureYear       | 4 digit year (i.e. 2008) manufacture year (3rd generation neoVI only)                                                                                        |
| unsigned chariBoardRevMajor          | Board revision major (3rd generation neoVI only)                                                                                                             |
| unsigned chariBoardRevMinor          | Board revision minor (3rd generation neoVI only)                                                                                                             |
| unsigned chariBootLoaderVersionMajor | Bootloader version major (3rd generation neoVI only)                                                                                                         |
| unsigned chariBootLoaderVersionMinor | Bootloader version minor (3rd generation neoVI only)                                                                                                         |
