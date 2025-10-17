The true power of CLI comes when we chain the commands together to build  command pipelines = very powerful workflows and pipelines. 
-	Different ways a command can take input and give output
-	Understand ways data flows into and out of commands – connect commands together to build powerful pipelines. 
-	Data streams can be redirected from their default locations to wherever you are so these are standard outputs, Standard Inputs and Standard Errors.– so you can direct the standard output of one command to the standard input of another. This process is called PIPING 

Standard Input (0) (data stream) + Command Arguments (not data stream) = Command applied = standard output (1) (data stream)+ standard error(2) (data stream). 
This means there are 4 total ways of getting data into and out of a command

2 ways for the command to get output (to cli or redirected) 
<img width="369" height="111" alt="p1" src="https://github.com/user-attachments/assets/2e37a59e-9b72-46f0-972e-223bd0a48512" />

  date command to run – output sent from data command and flows down standard output stream which is by default connected to our terminal screen therefore we see date below our command
You can redirect where the output data calls - REDIRECT
Error/ log – isn’t the primary output of the command, this is output into the screen as standard error to keep them separate eg below 
  - sends down standard error stream and outputs to the terminal
<img width="464" height="89" alt="p2" src="https://github.com/user-attachments/assets/a5ec6cee-c106-4f41-ba77-1a3b60035a5a" />

2 ways forthe  command to get input (from cli or from redirected)
-standard input – connected to the keyboard : eg cat 
 <img width="427" height="296" alt="p3" src="https://github.com/user-attachments/assets/bb25d1ef-b5d5-4864-92ec-07e31b00bce1" />
 
 basically means that if no file is give it will read from standard input and will appear right in our terminal 
 <img width="409" height="211" alt="p4" src="https://github.com/user-attachments/assets/a0577e91-7fc3-4204-ae06-f3aaeff95205" />

  control +C to get control back
Or we can tell the cat to read data/ redirect it to read data from a file or another data stream. 
WITH DATA STREAMS YOU CAN PASS THE STANDARD OUTPUT OF 1 DATA STREAM TO BE AN INPUT TO ANOTHER DATA STREAM– THEN PASS THE OUPUT OF THE 3RD TO THE 4TH ETC. – THIS RESULT SIN A VERY POWERFLU PIPELINE – IPORTANT CONCEPT AS IT MAKES WORKING WITH CLI VERY EFFECTIVE AND POWERFUL
Control + l to clear screen
Note how to update the command information
  <img width="602" height="144" alt="p5" src="https://github.com/user-attachments/assets/77ad3fe9-5c66-4761-b7ae-71f0d2946697" />

how to deal with a command that is not working – Notes it may not be installed on the Ubuntu by default and It is usually contained in the older versions- How to fix 
sudo apt update
sudo apt install (ncol) – it will install the packahge of what you want
then run your command again 
 <img width="602" height="316" alt="p6" src="https://github.com/user-attachments/assets/37f70a27-97ae-4911-8880-de8aa45d7394" />
<img width="496" height="246" alt="p7" src="https://github.com/user-attachments/assets/93b1f817-121d-4d05-aa40-52f632ed051d" />

 
but you can update and upgrade all options – by following this exact framework and it worked for me 
 <img width="602" height="180" alt="p8" src="https://github.com/user-attachments/assets/3b2564b0-9c42-4d8f-80a9-8b248aec4c16" />


Command line arguments
 <img width="602" height="396" alt="p9" src="https://github.com/user-attachments/assets/d439d525-8bab-41d9-92de-b04c60d3b4ec" />

Cal has 2 comand line arguments – one on A being 1 (after the date) so A has a command line argument and one on B so b had a command line argument– and 2 arguments for the overall cal command 12 and 2017

Diffrence bterrn command line arguments and data streams – is that  data streams can flow – redirected and piped together. Command line arguments only associate themselves with the commands dealing with at the moment. Data stre

Not all commands accept standard input = echo  command doesn’t bu majority do.You can Just check its man page and assume it cant accept if it doesn’t say

