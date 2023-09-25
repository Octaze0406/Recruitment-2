**HTML**
---

created a website using html .
learned commands such as {body,/body}- to describe the main content of the HTML.
 
{div,/div}- for grouping the contents of the web page to apply styles and fonts.

{p} -to write any content for user to read.

{em} will render the words in italic {/em}

{strong} will render the words as bold {/strong}

different levels of headings can be created using 
{h1}________{/h1}
{h2}_______{/h2}
.
.
.
{h6}___{/h6}

<elementName attributeName="attributeValue">Content</elementName>
element names can be <a , <img , <video
<a href"(for proving links)">_for writing content__________</a>
<img src="for link" alt="to provide descryption of image">
<video src="for link" width="" height="" contents(for play ,pause, stop contols over the video)

declaration at the begining is used to indicate 1. the type ofdocument 2. the version  eg:HTML 5, HTML4.01 strict, HTML 4.01 transitional, XHTML 1.0 Strict
eg; <!DOCTYPE html>
 To create HTML structure and content, we must add opening and closing <html> tags after declaring <!DOCTYPE html>:
  while the <body> displays info about the contents of web , the <head> above it tells us about the web page itself, not easily available for user.
   to provide a title to the web page use <title>____</title>

<body>
<a href="" target="_blank"> - to open the said link inside href in a new tab.
you can put your image as a link by simply putting the image command inside anchor :<a_____> <img________> </a>

TO HAVE THE user click a link and automatically scroll to that section ,
note:leave 2 spaces before starting the code on a differernt line if the code above is a parent code.

tp add a comment ; <!--________-->

TO CREATE A TABLE <table>
to create number of rows use <tr> </tr> --1 row
to fill it with date use <td>
to describe what the data represent we need table headings,,,<th>
First, a new row was added to hold the three headings
-- the use of the scope attribute, which can take one of two values:

row - this value makes it clear that the heading is for a row.
col - this value makes it clear that the heading is for a column.
format: <th scope="row/col" >___________</th>
we enclose different rows of the table under ,,,<thead>, <
tbody>, <tfoot>.

CSS -Cascading Style SHeets.

 a <form> that will send information to a location(____) as a POST request:

The (action) attribute determines where the information is sent.
The (method) attribute is assigned a HTTP verb that is included in the HTTP request.

eg: <form>
				<h1>heading</h1>  
	      <!--Add your code below-->
        <label for="username>Username</label> --shows near the inout box , what the user has to enter as input.
        <input type="text" name="username" value="Davie"> ,,,data stored as text under the name ;username
      </form>
     if we are asking the user for sesitive info and they dont want others to peek into their input typed on screen ;for password or pin 
we have type= "password"
for integers input 
<label for="year">Your age</label>
<input type="number" id="year" name="age" step="5">   <!-- step function provided a scroll wheel at the end of input box to input numbers in the multiples of 5>
if we want to set a range to how much number the user can input we use max="" and min="" along with type="range"
if you want to create a checkbox type input
<section class="protein">
 <label for="chicken">Chicken</label>
 <input type="checkbox" id="chicken" name="protein" value="chicken">
</section> creates a checkbox infront of chicken .

since checkbox creates multiples options to asnwer and if you want user to select only one option ,,,just change type="radio".
