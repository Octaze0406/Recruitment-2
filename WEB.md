**HTML{HYPERTEXT MARKUP LANGUAGE}**
--- 

Created a website using html . HTML-used for crating web pages.

**Commands I learned**
---

(<>) represented by ({}) for presenting in the repo.

+{body},{/body}- to describe the main content of the HTML.
 
+{div},{/div}- for grouping the contents of the web page to apply styles and fonts.

+{p} -to write any content for user to read. (p- indicates paragraph).

+{em} will render the words in italic {/em}

+{strong} will render the words as bold {/strong}

+different levels of headings can be created using - where the heirarchy ordering odf headings decreases from 1-6.

  ++{h1}________{/h1}
  
  +++{h2}_______{/h2}
  
  .
  .
  .
  
  +++++++{h6}___{/h6}

+{elementName attributeName="attributeValue">Content</elementName}

 ++element names can be {a(anchor) , {img , {video
 
+{a href"(for proving links)"}_for writing content__________{/a}

+{img src="for link" alt="to provide descryption of image"}

+{video src="for link" width="" height="" contents(for play ,pause, stop contols over the video)}

+declaration at the begining is used to indicate 

+_1. the type ofdocument _2. the version  eg:HTML 5, HTML4.01 strict, HTML 4.01 transitional, XHTML 1.0 Strict

+eg; {!DOCTYPE html}

+To create HTML structure and content, we must add opening and closing <html> tags after declaring {!DOCTYPE html}:

+while the {body} displays info about the contents of web , the {head} above it tells us about the web page itself, not easily visibile in the webpage for user.

+to provide a title to the web page use {title}____{/title}

+{body}
++{a href="" target="_blank"} - to open the said link inside href in a new tab.

++{a href="" target="_self"}- to open the said link inside the same tab.

+you can put your image as a - link by simply putting the image command inside anchor :{a_____} {img________} {/a}

+TO HAVE THE user click a link and automatically scroll to that section , first provide a anchor at begining and add the link href="#..." and at the part where you want to scroll to simpy put id="".

+note:leave 2 spaces before starting the code on a differernt line if the code above is a parent code.

+to add a comment ; {!--________--}

+TO CREATE A TABLE {table}

+to create number of rows use {tr} {/tr} --1 row [table row]

+to fill it with data use {td}

+to describe what the data represent we need table headings,,,{th}

+First, a new row was added to hold the three headings

++ the use of the scope attribute, which can take one of two values:

+++row - this value makes it clear that the heading is for a row.

+++col - this value makes it clear that the heading is for a column.

+format: {th scope="row/col" }___________{/th}

+we enclose different rows of the table under ,,,{thead}, {tbody}, {tfoot}.

++CSS -Cascading Style SHeets.

+a {form} that will send information to a location(____) as a POST request:

+The (action) attribute determines where the information is sent.

+The (method) attribute is assigned a HTTP verb that is included in the HTTP request.

+{!--Add your code below--}
        
+{label for="username Username{/label} --shows near the input box , what the user has to enter as input.
        
+{input type="text" name="username" value="Davie"} ,,,data stored as text under the name ;username
      +{/form}
      
+if we are asking the user for sesitive info and they dont want others to peek into their input typed on screen ;for password or pin 

+we have type= "password"

+for integers input 

+{label for="year"}Your age{/label}

{input type="number" id="year" name="age" step="5"}  {!-- step function provided a scroll wheel at the end of input box to input numbers in the multiples of 5}

+if we want to set a range to how much number the user can input we use max="" and min="" along with type="range"

+if you want to create a checkbox type input

Eg;
+{section class="protein"}
 
 {label for="chicken"}Chicken{/label}
 
 {input type="checkbox" id="chicken" name="protein" value="chicken"}
 
{/section} creates a checkbox infront of chicken .

+since checkbox creates multiples options to asnwer and if you want user to select only one option ,,,just change type="radio".

**CSS{CASCADING STYLE SHEETS**
---

CSS properties define how elements should be styled. For example, color, font-size, background-color, and margin are all properties.
+EG:
selector {
    property1: value1;
    property2: value2;
}

**SQL(STRUCTURED QUERY LANGUAGE)**
---

It is a language used to manage and manupulate data in databases. Hence it can be used to retreive, insert, delete data.

+So in wrong hands, it can easily be a way for attackers to expose and change the data of a database hence called as -SQL i injection attacks.

+Note= (--) makes after after this on the line of code render as comment and not as code.

***A.IMPACTS***
---

+SQL i impacts include revealing of sensitive data to attackers like:

 =passwords

 =credit card details

 =personal user details

***B.DETECTION***
---

+multiple sql injections can be found easily by using = Burp Scanner

+manually using

1. (') to look for eroor /anomolies
2. (' OR 1=1--) boolean conditions to look out for application responses.
3. ('; waitfor delay(0:0:20)-- )The purpose of injecting this code is to see if it's possible to manipulate the SQL query in a way that causes a time delay. If the delay occurs, it could be an indication that an SQL injection vulnerability exists in the application.

***C.WHERE DOES SQL INJECTION HAPPEN***
---

1. In SELECT statements in the WHERE query
2. In UPDATE statementsin the inserted values
3. In SELECT statements in row/column query.


**D.PREVENTION**
---

You don't write the specific details (user input) directly into the SQL query. Instead, you put placeholders (the blanks or checkboxes) where your preferences should go.



