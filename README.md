# class-10-reading

Class 10 notes Debugging

I. What when Wrong Troubleshooting JS. 
II. Types of errors<br>
  a. Syntax errors
    1. Spelling errors, that prevent your code from running. Usually provided an error message.<br>
    2. Logic Errors: errors where code does not preform the way you intended it to.<br> 
      a. i.e. program runs successfully but does not give result intended.<br>
III> Fixing syntax errors.<br>
  A. Error message examples and meanings.<br>
    1. Uncaught TypeError: guessSubmit.addeventListener is not a function: Something went wrong.<br>
      a. The function called is not recognized by the js interp usually means misspelled thing.<br> 
        1. Best to look it up in MDB search “mdn name-of-feture: <br>
    2. 2nd part number-game-errors.html:86:15 code error came from line 86 character 15 of the file number game errors<br>
IV.      Syntax errors round two<br>
  A. Uncaught TypeError: can’t access property “textContent”, loOrHi is null. (Firefox)<br>
  B. Uncaought Type Error: Cannot se properties of null (setting ‘textContent’) chromes. 
    1. Line is trying to se the textContent property of loOrHi variable to a string, does not contain what it is           suppose to<br>
    2. Looking though code loOrHi refer a class but when passed had no .dot so querySelector did not work.<br>
V.	Other common errors<br>
     A.   SyntaxError: missing ; before statement. <br>
	1. Error means you missed a semi colon at the end of one of your lines of code<br>
	2. Throws error because it thinks you are trying to do something different.<br>
		a. Double check assignment operators. <br>
     B.    SyntaxError: missing : after property id:<br>
	1. Usually relates to an incorrectly formed JS object. <br>
     C.   Missing } after function body means you missed a curly braces from function or 				condition structure. <br>
     D. SyntaxError: expected expression got ‘string’ or Syntaxerror: unterminated string literal.<br>
	1. Generally mean a forgotten an opening or closing ‘ of a string value.<br> 
	2. String would be replaced with  an unexpected character.<br> 
	3. Second Error means the string has not been ended with a quote mark.<br> 


Javascript Debugger

I. How to open dev tools in your browser<br>
  A. Can use short cut command + option + I <br>
  B. Chrome more tools -> developer tools <br>
II. The inspector: DOM explorer and CSS editor<br>
  A. Shows what the HTML on page looks like at runtime as well as what css is applied<br>
	to each element on the page.<br> 
      B. Allows you to instantly modify the html and css and the the results of your changes<br>
	selected live. 
III. Exploring the DOM inspector<br> 
      A. Right click an html element in the Dom inspector and look at the the context menu.<br>
	1.Delete Node deletes current element<br>
	2. Edit as HTML (add attribute/edit text) lets you change the HTML and see results<br>
	     right away<br>
	3. :hover/:active/:focus forces element state to be toggled on.<br>
	4. Copy/Copy as HTML copy the currently selected HTML copy the currently selected 			     HTML<br>
IV. Exploring the CSS Editor<br>
     A. Default the css editor displays the css rules applied to the currently selected 			         	element<br>
     B. Features are handy for following<br>
	1. Rules applied to current element shown in order of most to least specific<br>
	2. Chick checkboxes next to declaration to see what would happen if you removed 			     it<br>
	3. Click little arrow next to each short next to each shorthand prop to sow the props 			    longhand<br>
	4. Next to each rule is the filename and line number th rule is defined in. Clicking rule 			    causes dev tools to just to show it on it’s own view. 
     C. Number of clickable tabs at the top of the css viewer<br>
	1. Computed: this shows the computed styles for the currently selected element<br>
	2 Layout: in firefox this are included two sections<br>
		a. Box model reps visually the current elements box model, can see<br> 					    padding, border, & margin is applied to and how big content is<br>
		b. Grid if pan uses css grid this section will allow you to see grid details<br>
		c. Fonts: in Firefox the fonts tab shows the fonts applied to current element<br>

V. The Javascript debugger<br>
       A. Debugger allows watching othe value of variables, set breakpoints, places in<br> 			your code you want to pause execution and identify the problem that prevent <br>
	 code from executing properly<br>

  B. File list<br>
	A. First pant on left contains the list of files associate with the page you are debugging
	B. Select the file you want to work on.<br>
	C. Source Code<br>
		1. Set breakpoints with yo want to pause execution <br>
	D. Watch expressions and breakpoints<br>
		a. Watch espresso shows that the listItems variable has been added. Can<br>
		    expand the list to view values array. <br>
	E. Breakpoints. <br>
	F. Call stack.. Shows you what code was execute to get to the current line. <br>
	G. Scopes, how’s values visible from various points within your code<br>

VI. The javascript Console. <br>
	A. Allows to run lines of js against  the page currently loaded in the browser. 

Name Some Key Differences between a syntax Error and an Logic Error.
	a. A syntax error is something like a spelling error, or a misplaced curly brace. A logic error is an error that happens when your code works but is producing the wrong output. 

2. Name a few types of errors you have encountered in pas lab assignments and explain how you were able to correct them. 
	a. What a good question. I feel like I have had so many errors, one of them included a mime error which was that I could not get my stylesheet and my reset to be found because they were not in the correct file. I know I have missed some curly braces along the way. I will say one thing that I am finding quite difficult about js at the moment is that the code doesn’t break so to speak when there is a problem do don’t get a lot of end of line errors when you forget something and your code just doesn’t work. I have had many logic errors. I have one right now that my code is producing something but its coming up as undefined. However if I remember right in the console log it’s getting put into the correct array. 

3. How will this topic continue to influence your long term goals? 
	a. Debugging is a super important part of programming. I think the greater question here is how will it not influence my long term goals. I mean you save time to go looking for bugs at some point right? And bugs are reported? So seems like a pretty big deal. 

How would you describe a javascript debugger tool and how it works to someone just starting out in software development. 
	a. The JS debugger is tool, that comes built into to chrome, firefox, etc. That makes it easier to find your mistakes. It runs though your code and when it hits a problem it tells you where it is based on line and character. Not only does it do this, but you can also set up breakpoints to run your code to a certain point to discover if it is running as you expect. You can step into that part of code and get a closer look at what’s really going on. It is a very good tool to get to know to work out some possible logic issue you may run into so you aren’t just banging your head against a wall trying to fix them. 

2. Define what a breakpoint is. 
	a. A breakpoint is a point you set in your sources section of the debugger that will run your code to that point. It make is easier to find out if your code is working as you expect. 

3. What is the call stack. 
	a. A call stack show you what code has been executed to get you to the line of code you have a breakpoint on. 



## Things I want to learn more about
  how to be more confident in using the debugger and understand JS error codes. 

     
