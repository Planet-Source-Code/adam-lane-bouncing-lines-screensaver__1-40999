<div align="center">

## Bouncing Lines ScreenSaver

<img src="PIC200211231748394304.gif">
</div>

### Description

This is a really cool ScreenSaver, it looks like a bunch of lines following eachother and bouncing off the sides of your screen. It is a clone of the windows screensaver. You can change the speed and color of the lines. Enjoy
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Adam Lane](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/adam-lane.md)
**Level**          |Intermediate
**User Rating**    |5.0 (15 globes from 3 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Graphics](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/graphics__1-46.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/adam-lane-bouncing-lines-screensaver__1-40999/archive/master.zip)





### Source Code

<p><b><u><font face="Verdana"><small><small><small><small><small><small><small>Bouncing
Lines ScreenSaver</small></small></small></small></small></small></small></font><small><small><small><small><small><font face="Verdana"><small><small><br>
</small></small></font></small></small></small></small></small></u><font face="Courier New"><small><small><small><small><small><font face="Verdana"><small><small>by
Adam Lane</small></small><br>
<br>
</font></small></small></small></small></small>
</font>
</b><font face="Courier New"><font face="Verdana"><small><small><small><small><small><small><small>1) Create a
</small></small></small></small></small></small></small></font>
</font><font face="Verdana"><small><small><small><small><small><small><small>borderless
</small></small></small></small></small></small></small></font><font face="Courier New"><small><small><small><small><small><small><small><font face="Verdana">form and a timer<br>
2) Form1 and Timer1<br>
3) Copy this code into your form</font></small></small></small></small></small></small></small><small><small><small><small><small><small><small><small><small><br>
<br>
</small></small></small></small>Dim x(4), Y(4), xSpeed(4), ySpeed(4), Trails As Integer<br>
<br>
Private Sub Form_Load()<br>
&nbsp;&nbsp;&nbsp; Form1.WindowState = vbMaximized<br>
&nbsp;&nbsp;&nbsp; Form1.BackColor = vbBlack<br>
&nbsp;&nbsp;&nbsp; Form1.ForeColor = vbBlack<br>
&nbsp;&nbsp;&nbsp; Form1.FillColor = vbBlack<br>
&nbsp;&nbsp;&nbsp; Timer1.Interval = 1<br>
&nbsp;&nbsp;&nbsp; For i = 0 To 3<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; x(i) = Form1.ScaleWidth \ 2<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Y(i) = Form1.ScaleHeight \ 2<br>
&nbsp;&nbsp;&nbsp; Next i<br>
&nbsp;&nbsp;&nbsp; xSpeed(0) = -150: xSpeed(2) = -150<br>
&nbsp;&nbsp;&nbsp; xSpeed(1) = 70: xSpeed(3) = 70<br>
&nbsp;&nbsp;&nbsp; ySpeed(0) = -105: ySpeed(2) = -105<br>
&nbsp;&nbsp;&nbsp; ySpeed(1) = 90: ySpeed(3) = 90<br>
&nbsp;&nbsp;&nbsp; Trails = 50<br>
End Sub<br>
<br>
Private Sub Timer1_Timer()<br>
&nbsp;&nbsp;&nbsp; Dim z As Integer<br>
&nbsp;&nbsp;&nbsp; If Trails > 0 Then<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Trails = Trails - 1<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; z = 1<br>
&nbsp;&nbsp;&nbsp; Else<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; z = 3<br>
&nbsp;&nbsp;&nbsp; End If<br>
&nbsp;&nbsp;&nbsp; For i = 0 To z<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; x(i) = x(i) + xSpeed(i)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Y(i) = Y(i) + ySpeed(i)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; If x(i) < 0 Or x(i) > Form1.ScaleWidth Then xSpeed(i) =
-xSpeed(i)<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; If Y(i) < 0 Or Y(i) > Form1.ScaleHeight Then ySpeed(i) =
-ySpeed(i)<br>
&nbsp;&nbsp;&nbsp; Next i<br>
&nbsp;&nbsp;&nbsp; Line (x(0), Y(0))-(x(1), Y(1)), vbBlue<br>
&nbsp;&nbsp;&nbsp; Line (x(2), Y(2))-(x(3), Y(3)), vbBlack<br>
&nbsp;&nbsp;&nbsp; DoEvents<br>
End Sub<br>
</small></small></small></small></small>
</font></p>

