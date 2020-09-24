<div align="center">

## OPTIMISED circular collision detection \-100% performance speed upgrade from most traditional methods


</div>

### Description

This code performs a collission-detection calculation between two circles using some really basic trig. Usefull for games... Performance much higher than traditional circle-collision detection... only takes 45% the amount of time to do the same thing as most circle collision detection functions!!! thats over 100 percent performance increase. Just thought it'd be usefull to game programmers and such...

I bet your wondering "What did this guy do to speed things up so much?" Well thats plain and simple!!! I just replaced the (A)^2 part of the equation, where A = Y2 - Y1 or X2 - X1, with A * A, because its ALOT faster... just doing that, AND storing A in its own variable, speeds things up ALOT, it only takes aprox 45% of the time to do the same collision dectection task!!! Woopty-Dooo!!!! =)
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[\(Tim Miron\) yar\-interactive software](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/tim-miron-yar-interactive-software.md)
**Level**          |Intermediate
**User Rating**    |5.0 (10 globes from 2 users)
**Compatibility**  |VB 4\.0 \(16\-bit\), VB 4\.0 \(32\-bit\), VB 5\.0, VB 6\.0
**Category**       |[Games](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/games__1-38.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/tim-miron-yar-interactive-software-optimised-circular-collision-detection-100-performance-__1-27931/archive/master.zip)





### Source Code

```
'USE THIS in place of your regular
'circle collision detection function
'Only takes APROX. 45% of the time of
'traditional circle collision dectect
Public Function OptCircCollide(X1 As Long, _
Y1 As Long, X2 As Long, Y2 As Long, _
R1 As Long, R2 As Long) _
As Boolean
Dim X2mX1 As Long 'pre-calculate x2 - x1
Dim Y2mY1 As Long 'pre-calculate y2 - y1
X2mX1 = X2 - X1
Y2mY1 = Y2 - Y1
'calculate distance between 2 points on
'a X-Y grid:
If Sqr((X2mX1 * X2mX1) + (Y2mY1 * Y2mY1)) _
<= R2 + R1 Then OptCircCollide = True
End Function
```

