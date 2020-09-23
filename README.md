<div align="center">

## \_Screen Freeze JOKE


</div>

### Description

a cool little joke that makes it look like the screen is froze, and it stays on top so nothing works. please **VOTE**!!!!

to use the code set the selected form's borderstyle to none, then insert code, then run it. just click to get out of the prog
 
### More Info
 
open the prog


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[poop\_4\_brains](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/poop-4-brains.md)
**Level**          |Beginner
**User Rating**    |3.8 (65 globes from 17 users)
**Compatibility**  |VB 6\.0
**Category**       |[Jokes/ Humor](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/jokes-humor__1-40.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/poop-4-brains-screen-freeze-joke__1-32939/archive/master.zip)





### Source Code

```
'Screen Freeze Joke
'by Kevin Fleet
'March 21, 2002
'(KEVCOM)
'******************
'api functions to draw
Private Declare Function GetDC Lib "user32" ( _
  ByVal hwnd As Long) As Long
Private Declare Function BitBlt Lib "gdi32" ( _
  ByVal hDestDC As Long, _
  ByVal X As Long, _
  ByVal Y As Long, _
  ByVal nWidth As Long, _
  ByVal nHeight As Long, _
  ByVal hSrcDC As Long, _
  ByVal xSrc As Long, _
  ByVal ySrc As Long, _
  ByVal dwRop As Long) As Long
Private Sub Form_Load()
Me.AutoRedraw = True 'so that the screen's image stays on the form
Me.Left = 0 'set the size
Me.Top = 0
Me.Width = Screen.Width
Me.Height = Screen.Height
BitBlt Me.hDC, 0, 0, Screen.Width, Screen.Height, GetDC(0), 0, 0, vbSrcCopy
'copy the screens image onto the form so it will look frozen
Me.Visible = True
Do 'loop the stay on top thing so its always on top
Me.ZOrder 0
DoEvents
Loop
End Sub
'REMOVE THIS FOR ACTUAL USE OF JOKE \/ (so the user cant get out)
Private Sub Form_MouseDown(Button As Integer, Shift As Integer, X As Single, Y As Single)
End 'this is here so you can try the code and still vote afterwards
'to make it even better disable ctrl+alt+del and alt+f4
'get api to keep the form ontop
End Sub
```

