# alireza.khazae
پروژه ماشین حساب
private void numberButton_Click(object sender, EventArgs e)
 2 {
 3     Button sourceButton = (sender as Button);
 4     double oldNumber, buttonNumber, newNumbernewNumber;
 5  
 6     if (shouldClear)
 7     {
 8         outputTextBox.Clear();
 9         oldNumber = 0;
10         shouldClear = false;
11     }
12     else
13     {
14         oldNumber = Double.Parse(outputTextBox.Text);
15     }
16  
17             
18     buttonNumber = Double.Parse(sourceButton.Text);
19     newNumbernewNumber = (oldNumber * 10) + buttonNumber;
20  
21     if (isFirst)
22     {
23         firstOperand = newNumbernewNumber;
24     }
25     else
26     {
27         secondOperand = newNumbernewNumber;
28     }
29  
30     outputTextBox.Text += sourceButton.Text;
31  
32     Calculate(symbol);
33 }
