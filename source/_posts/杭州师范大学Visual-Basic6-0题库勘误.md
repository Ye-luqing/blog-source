title: 杭州师范大学Visual Basic6.0题库勘误
date: 2015-06-19 22:17:06
categories:
- 计算机
- Visual Basic6.0
tags:
- Visual Basic6.0
- 杭州师范大学
- 勘误

---
Visual Basic6.0是我这个学期最后一门要通过的课,通过了我就毕业了.学校的正式考试题目是从15套题里抽取的,[15套题及其参考答案在此](/img/杭州师范大学Visual Basic6.0题库及其参考答案.zip).因此我考前认真刷学校的题库.我的刷题记录在此:[填空题刷题记录](/img/杭州师范大学Visual Basic6.0题库部分填空题解答_by叶卢庆.zip),[设计题刷题记录](/img/杭州师范大学Visual Basic6.0题库部分设计题解答_by叶卢庆.zip).我的刷题记录中,设计题和填空题的解答,文件的编号比较混乱,没有时间和精力重新整理了,因此读者最好不要看我的刷题记录.学校的15套题及其参考答案对于在杭师读书并且要考VB的同学来说,或许倒是值得一看.

在刷题库的过程里,我发现学校的一些题目或参考答案出了问题,罗列如下.随着我刷题进度不断向前推进,该列表会逐渐添加.当然由于我水平和精力有限,不太可能挑出所有的错.

需要指出的是,有些填空题的参考答案有问题,不是指填空题所给出的参考答案是错的,而是这些填空题所给出的答案没有罗列出所有常见的可能情况.再加上学校的填空题是机改的,这样就造成有些学生即使填了正确的答案,但是由于和参考答案不符,也会被机器判错.

这是个比较大的缺陷,等我考完成绩出来后会和老师反映.希望学校能对我指出的缺陷进行修正.另外,一个比较好的解决方案或许是改卷老师重新检查考了不及格的人的VB填空题答案,如果发现机器存在误判现象,则加以纠正.

# 选择题勘误

## 第1套题选择题7
设置命令按钮cm1的背景色为红色，可以执行语句______。
A. cm1.BackColor=vbred

B. cm1.BackColor = vbred: cm1.style=1

C. cm1.Picture = RGB(255, 0, 0)

D. cm1.BackColor = RGB(255, 0, 0):cm1.enabled=True

答案是B.

然而,当我在代码窗口中实际敲入B时,运行时程序警告:不能给只读属性赋值.经过百度,我发现cm1.style=1是错的,因为cm1的style属性是只读属性,只可以一开始就在属性窗口中设置,而不能在代码中设置.见[该链接](http://zhidao.baidu.com/question/646462958330129165.html?qbl=relate_question_3&word=command1.style%3D1).

## 第8套题选择题7
与第1套题选择题7完全一样.

## 第9套题选择题8
与第1套题选择题7完全一样.
#填空题勘误

## 第5套题程序填空题1
以下程序执行后将产生一个6×6的转置矩阵，将二维数组中所有行和对应列的元素进行交换。
```
Private Sub Form_Click()
    Dim a(1 To 6, 1 To 6) As Integer
    Dim i As Integer, j As Integer
    Form1.Print "原始数据"
    For i = 1 To 6
        For j = 1 To 6
            a(i, j) = Int(Rnd * 10)
            Form1.Print a(i, j);
        Next j
        Form1.Print
    Next i
    For i = 2 To 6
        For j = 1 To ----- 1 -----
            ------ 2 -----
        Next j
    Next i
    Form1.Print "转置后数据"
    For i = 1 To 6
        For j = 1 To 6
            ----- 3 -----
        Next j
        Form1.Print
    Next i
End Sub
Public Sub Swap(a As Integer, b As Integer)
    Dim temp As Integer
    temp = a
    a = b
    b = temp
End Sub
```

参考答案是:
1.I
2.Call Swap(a(I,j),a(j,I)) 或者 Swap(a(I,j),a(j,I))
3.Print  a(i,j)

然而,对于第1空来说,其实填 I-1 也是可以的.这两种填法是等效的.因为参考答案转置一个矩阵的时候,对角线上的元素和自己进行了交换(Swap),然而这是多此一举.


## 第6套题程序填空题2
程序运行后，鼠标多次在图片框内拖动后，绘制出多个绿色边框矩形，填充样式在“实心”、“透明”间交替变换。
```
----1----
Private Sub Picture1_MouseDown(Button As Integer, _
      Shift As Integer, X As Single, Y As Single)
    x0 = X: y0 = Y
End Sub
Private Sub Picture1_MouseUp(Button As Integer, Shift As Integer, _
     X As Single, Y As Single)
    If ----2----Then
        Picture1.FillStyle = 0
    Else
        Picture1.FillStyle = 1
    End If
    ----3----
End Sub
```
参考答案:
1.Dim x0 as single,y0 as single 或者 Dim x0!,y0!
2.Picture1.Fillstyle &lt; &gt; 0 或者 Picture1.Fillstyle=1
3.Picture1.line (x0,y0)-(X,Y),RGB(0,255,0),B 或者 Picture1.line (x0,y0)-(X,Y),vbgreen,B

然而,第3空的参考答案还漏掉了很多种情形,即 Picture1.line (X,Y)-(x0,y0),RGB(0,255,0),B 或者 Picture1.line (X,Y)-(x0,y0),vbgreen,B 或者Picture1.line (x,y0)-(x0,y),RGB(0,255,0),B 或者 Picture1.line (x,y0)-(x0,y),vbgreen,B 或者 Picture1.line (x0,y)-(x,y0),RGB(0,255,0),B 或者 Picture1.line (x,y0)-(x0,y),vbgreen,B 等等等等.当然,如果题目加上限制条件"鼠标按下、抬起的位置分别为矩形斜对角线的顶点"的话(就像第11套题程序填空题2一样,见下面),后4种情形可以去掉.

## 第6套题程序填空题3
下列程序运行时，单击Command1(0)后，清空组合框原有内容，从外部文件中读入的数据显示在组合框中，如图所示。单击Command1(1)后，将组合框中的各表项输出到外部文件；单击Command1(2)后，将组合框中文本框部分的文本添加作为组合框的表项；单击Command1(3)后，将组合框中选中的表项删除。
![图1](/img/杭州师范大学Visual-Basic6-0题库勘误-1.png)
```
Private Sub Command1_Click(Index As Integer)
    Select Case Index
    Case 0
        ----1----
        Open "d:\aaa.txt" For Input As #1
        Do While Not EOF(1)
            Line Input #1, a$
            Combo1.AddItem a$
        Loop
        Close #1
    Case 1
        Open "d:\aaa.txt" For Output As #1
        For I% = 0 To ----2----
            Print #1, Combo1.List(I%)
        Next I%
        Close #1
    Case 2       '添加
        Combo1.AddItem ----3----
    Case 3       '删除
        ----4----
    End Select
End Sub
```
参考答案:
1.combo1.clear
2.combo1.listcount-1
3.combo1.text
4.Combo1.RemoveItem Combo1.ListIndex

然而,第4空其实填 Combo1.RemoveItem (Combo1.ListIndex) 也是可以的.

## 第7套题程序填空题3
文本文件“C:\mydoc\zg.txt”包括工资、职务情况，每条记录由工号、工资、职称组成，现对文件内容进行修改，即对不同职称的职工增加工资，规定高级职称的增加15%，中级职称的增加10%，初级的增加5%，其他人员不加工资。
```
Pirvate Sub cmdModif_Click()
Dim num As Integer, gz As Single, zc As String  ‘ 定义工号、工资、职称的变量名和类型
 Open ” C:\mydoc\zg.txt” For Input As #1
 Open ” C:\mydoc\lszg.txt” For Output As #2
 Do While Not EOF(1)
  ----1----
  Select Case zc
   Case “高级”
   gz = gz*1.15
   Case “中级”
   gz = gz*1.1
   Case “初级”
   gz = gz*1.05
  End Select
  Write #2, num, gz, zc 
 Loop
 Close #1,#2
 Open ” C:\mydoc\lszg.txt” ----2----As #1
 Open ” C:\mydoc\zg.txt”for output As #2
 Do While Not EOF(1)
  Input #1, num, gz, zc
  ----3----
 Loop
 ----4----
End Sub
```
首先值得指出的是,题目中所有的引号都使用了中文的引号,这在VB里编译是通不过的,因此要把所有的中文引号改成英文引号,变成如下
```
Pirvate Sub cmdModif_Click()
Dim num As Integer, gz As Single, zc As String  '定义工号、工资、职称的变量名和类型
 Open "C:\mydoc\zg.txt" For Input As #1
 Open "C:\mydoc\lszg.txt" For Output As #2
 Do While Not EOF(1)
  ----1----
  Select Case zc
   Case "高级"
   gz = gz*1.15
   Case "中级"
   gz = gz*1.1
   Case "初级"
   gz = gz*1.05
  End Select
  Write #2, num, gz, zc 
 Loop
 Close #1,#2
 Open "C:\mydoc\lszg.txt" ----2----As #1
 Open "C:\mydoc\zg.txt"for output As #2
 Do While Not EOF(1)
  Input #1, num, gz, zc
  ----3----
 Loop
 ----4----
End Sub
```
一些其它的题目也有类似的问题,在此不一一指出了.其次,由于现实中的工号往往比较长,经常会超出integer数据类型的范围,因此最好把题目中的Dim num as integer改成 Dim num as long.

参考答案是:
1.Input  #1,num,gz,zc
2.For Input
3.Write  #2,num,gz,zc

然而,第3空其实写成 Print  #2,num,gz,zc也是可以的,这一点参考答案没有考虑到.

## 第8套题程序填空题2
该程序的功能为：从1到1000中找出这样的数，该数每位上数字的阶乘之和等于该数，并将结果输出从窗体输出。
```
Private Sub Form_Click()
    Dim k, a, n, I, m
    Dim p As Integer
    For k = 1 To 10000
        a = Ltrim(Str(k))
        n = 0
        m = Len(a)
        For I = 1 To ----1----   
            p = Val(Mid(a, I, 1))
            n = ----2---- 
        Next I
        If n = k Then Form1.Print k
    Next k
End Sub
Function fact(x As Integer) As Long
  '该函数用于计算阶乘
    Dim y As Long
    Dim I%
    y = 1
    For I = 1 To x
        y = y * I
    Next I
    ----3----
End Function
```
参考答案略.题目的问题是 Dim k, a, n, I, m 应该改成 Dim k,a,n,I,m as integer

## 第9套题程序填空题2
以下程序产生n个两位随机整数，将其中个位数等于5的数存入数组B中，并以每行五个的紧凑格式在窗体中用输出，同时输出该数组的个数。
```
Private Sub Form_Click()
    Dim a() As Byte, b() As Byte
    Dim i As Byte, m As Byte, n As Byte
    n = InputBox("请输入n值：")
    ----1---- a(n), b(n)
    For i = 1 To n
        a(i) = 10 + Int(Rnd * 90)
        If a(i) Mod 5 = 0 Then
            m = m + 1
            ----2----
        Print b(m);
        If ----3----
        End If
    Next i
    Print
    Print "个位数为0的数有"; m; "个"End Sub
```
参考答案略.首先,该题最后的End Sub不能和其它代码写在同一行上,否则不能编译通过.其次,倒数第2句里,"个位数为0的数有"应该改成"个位数为5的数有".

## 第9套题程序填空题3
本程序通过选项来修饰预览区文字。单击字体组合框Cboziti可以设置预览区域的标签文字label5的字体；单击字号组合框Cbozihao可以设置预览区域的标签文字的字形；选择删除线复选框可以设置是否加删除线。
![图2](/img/杭州师范大学Visual-Basic6-0题库勘误-2.png)
```
Private Sub Cbozihao_Click() '选择字号
Label5.FontSize = ----1----
End Sub
Private Sub Cbozihao_ ----2---- () '输入选项中没有的字号
If Val(Cbozihao.Text) > 0 And Val(Cbozihao.Text) < 72 Then
    Label5.FontSize = Val(Cbozihao.Text)
Else
    Label5.FontSize = 9
End If
End Sub
Private Sub Cboziti_click()’字体
----3----
End Sub
Private Sub Check1_Click()‘复选框删除线
If  ----4----  Then
    Label5.FontStrikethru = True
Else
    Label5.FontStrikethru = False
End If
End Sub
```
参考答案是
1.cbozihao.text
2.change
3.label5.fontname=cboziti.text
4.check1.value=1 或 1=check1.value

然而,第1空其实还可以填 cbozihao.List(cbozihao.ListIndex) 或者 cbozihao.list cbozihao.listindex 或者 Val(Cbozihao.Text) (之所以考虑这个选项,是因为Val(Cbozihao.Text)在后面确实真切地出现了,这会影响很多考生的选择)

## 第11套题程序填空题2
程序运行后，在图片框控件Pic1上拖动鼠标，绘制出一个矩形。鼠标按下、抬起的位置分别为矩形斜对角线的顶点，矩形轮廓线为红色，矩形内部填充色为绿色。
```
----1----
Private Sub Pic1_MouseDown(Button As Integer, Shift As Integer, X As Single, Y As Single)
    x1 = X:  y1 = Y
End Sub
Private Sub Pic1_MouseUp(Button As Integer, Shift As Integer, X As Single, Y As Single)
    Pic1.FillColor = vbGreen
    ----2---- 
    ----3---- 
End Sub
```
首先,题目中说的"斜对角线"就是指"对角线".参考答案如下:
1.Dim x1 as single,y1 as single 或者 Dim x1!,y1!
2.Pic1.Fillstyle=0
3.Pic1.line (x1,y1)-(x,y),vbred,B 或者 Pic1.line (x1,y1)-(x,y),255,B 或者 Pic1.line (x1,y1)-(x,y),RGB(255,0,0),B 

然而,对于第2空来说,可以填Pic1.Fillstyle=M,其中M可以是很多其它的字符.比如你在第2空填 Pic1.Fillstyle=hahahaha,画出来的也是实心的!

而且对于第3空来说,也可以为 Pic1.line (x,y)-(x1,y1),vbred,B 或者 Pic1.line (x,y)-(x1,y1),255,B 或者 Pic1.line (x,y)-(x1,y1),RGB(255,0,0),B

## 第12套题程序填空题1
本程序是将列表框List1与List2中各表项合并到List3：List1与List2中原有各表项已按ASCII码从大到小排列。要求合并后List3中各表项也要从大到小排列。
```
 Private Sub Command1_Click()
      Dim I as integer,j as integer
   List3.Clear
  ----1----
     If List1.ListCount * List2.ListCount = 0 Then Exit Do
     If----2----Then
      List3.AddItem List1.List(0): List1.RemoveItem (0)
     Else
      List3.AddItem List2.List(0): List2.RemoveItem (0)
     End If
   Loop
   For i= 0 To List1.ListCount – 1
     List3.AddItem List1.List(i)
   ----3----
   For j = 0 To List2.ListCount - 1
     List3.AddItem List2.List(j)
   Next j
   List1.Clear: List2.Clear
 End Sub
 ```
 参考答案:
 1.Do
 2.list1.list(0)>list2.list(0) 或者 list2.list(0)< list1.list(0)
 3.next i
 
然而,第2空填 list1.list(0)>=list2.list(0) 或者 list2.list(0)=< list1.list(0) 也可以.

## 第12套题程序填空题2
下列程序运行时，先输入各公司月销售额，然后单击命令按钮，图片框中用红、绿、蓝色显示A、B、C公司销售额的圆饼图（如下图所示）。
![图3](/img/杭州师范大学Visual-Basic-6-0题库勘误-3.png)
```
Private Sub Form_Load()
    Picture1.Width = Picture1.Height
End Sub
Private Sub Command1_Click()
    Const PI = 3.141593
    Dim a As Single, b As Single, c As Single, x As Single
    Picture1.Scale (-8, -8)-(8, 8)
    ----1---- 
    a = Text1(0).Text: b = Text1(1).Text
    c = Text1(2).Text
    x =----2---- 
    Picture1.FillColor = RGB(255, 0, 0)
    Picture1.Circle (0, 0), 6, 0, ----3---- 
    Picture1.FillColor = RGB(0, 255, 0)
    Picture1.Circle (0, 0), 6, 0, -a * x, -(a + b) * x
    Picture1.FillColor = vbBlue
    Picture1.Circle (0, 0), 6, 0, -(a + b) * x, -(a + b + c) * x
End Sub
```
参考答案是
1.Picture1.fillstyle=0
2.2\*PI/(a+b+c) 或者 PI\*2/(a+b+c)
3.-2\*PI,-a\*x

然而,对于第1空来说,可以填Pic1.Fillstyle=M,其中M可以是很多其它的字符.比如你在第1空填 Pic1.Fillstyle=hahahaha,画出来的也是实心的!在第2空里,其实a+b+c用a+c+b或b+c+a或b+a+c或c+a+b或c+b+a替掉也可以.第3空中-2\*PI可以改成 -Pi\*2,-a\*x可以改成-x\*a 等等.

## 第14套题程序填空题3
以下程序运行时，打印输出一个如图所示的菱形图案。
![图4](/img/杭州师范大学Visual-Basic-6-0题库勘误-4.png)
```
Private Sub Command1_Click()
    Dim I As Integer,j As Integer, n As Integer
    Form1.Cls
    For I = 1 To 9
     If I <= 5 Then '打印上半部
       Print ----1---- '定位
       For j = 1 To ----2----
         Print "*";
       Next j
       Print
     Else
      Print Spc(I - 5);
      For j = 1 To ----3----
        Print "*";
      Next j
      ----4----
     End If
    Next I
End Sub
```
参考答案是
1.spc(5-i); 或者 Tab(5-I+1); 或者 Tab(6-I)
2.2\*I-1 或者 I\*2-1
3.2\*(10-I)-1 或者 (10-I)\*2-1 或者 19-2\*I 或者 19-I\*2
4.print

然而,第1 空还可以填space(5-i);

## 第15套题程序填空题3
以下程序运行时，计算下列级数的和，直到累加的末项之绝对值小于10的-7次方为止。
$$
1-x+\frac{x^2}{2!}-\frac{x^3}{3!}+\frac{x^4}{4!}-\cdots
$$
```
Private Sub Command1_Click()
     Dim s As Double, x As Double, t As Double, I As Integer
     x = InputBox("x=")
     s = 1
     I = 1
     t =----1----
     Do While ----2----<1e-7
       t = -t * ----3----
       I = I + 1
       s=----4----
     Loop
     Print s
End Sub
```
参考答案是
1.1
2.Abs(t)
3.x/i
4.s+t 或者 t+s

然而,另外一组答案亦可行
1.1
2.abs(x^(i-1)/t)
3.i
4.s+x^(i-1)/t 或者 x^(i-1)/t+s
