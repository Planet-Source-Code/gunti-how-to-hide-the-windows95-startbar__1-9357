<div align="center">

## How to hide the Windows95\-Startbar


</div>

### Description

This shows an easy way, how to hide window's 95/98 Startbar.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[gunti](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/gunti.md)
**Level**          |Intermediate
**User Rating**    |4.5 (18 globes from 4 users)
**Compatibility**  |VB 3\.0, VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0, VB Script, ASP \(Active Server Pages\) 
**Category**       |[Windows API Call/ Explanation](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/windows-api-call-explanation__1-39.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/gunti-how-to-hide-the-windows95-startbar__1-9357/archive/master.zip)

### API Declarations

```
'copy this in a module:
Dim hwnd1 As Long
Declare Function SetWindowPos Lib "user32" _
    (ByVal hwnd As Long, ByVal hWndInsertAfter As Long, ByVal x As _
    Long, ByVal y As Long, ByVal cx As Long, ByVal cy As Long, ByVal wFlags _
    As Long) As Long
Declare Function FindWindow Lib "user32" _
    Alias "FindWindowA" (ByVal lpClassName As String, ByVal lpWindowName _
    As String) As Long
```


### Source Code

```
'this is for the form; ->
Private Sub Command1_Click()
  hwnd1 = FindWindow("Shell_traywnd", "")
  Call SetWindowPos(hwnd1, 0, 0, 0, 0, 0, &H80)
End Sub
Private Sub Command2_Click()
  hwnd1 = FindWindow("Shell_traywnd", "")
  Call SetWindowPos(hwnd1, 0, 0, 0, 0, 0, &H40)
End Sub
```

