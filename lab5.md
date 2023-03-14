<h1> Revisiting Lab Report 3 </h1>
                                 
<p>Lab report 3 was fascinating to me because it gave me better insight into the way the grep command
worked. It is arguably one that I have used time-and-time again during this course. For this lab report,
I want to explore four different command line options for the <code>less</code> command.</p>


<h2><code>-N</code> Displays number on each line of the output.</h2>
<p>Here is the syntax for the command:
  <code>less -N [filename] </code>
    Filename is the name of the file we want to view, and less will display what is inside, with the 
    line numbers on the left side. <br>
  <b> *** WARNING: "-N" needs to be captialized! ***</b>
    </p>
<h3>Example 1:</h3>
Command run:
<code>less -N ch1.txt</code>
  
      
<h4>Output:</h4>
      
![image](1photo/np1.png)
      
<p>This opens the ch1.txt file and shows the line number on the left of the screen.</p>
<h3>Example 2:</h3>
Command run:
      
<code> less -N ch4.txt </code>
      
<h4>Output:</h4>
      
![image](1photo/np2.png)
      
<p> This is a good example of what it looks life if the line is exmpty. It still counts it as a space.
How cool!</p>
  
<h2><code>-i</code>Allows for case-insensitive search within a tex file</h2>
<p>Here is the syntax for the command:
  <code>less -i [filename] </code>
    Filename is the name of the file we want to view, and less will display what is inside, with the 
    option to search. Once less is open you type:<br>
<code>-i</code>
<p>This enables ignore case in search. Here is the syntax for search:</p>
<code>/< phrase ></code>

  
  <b> *** WARNING: "-i" needs to be lowercase! ***</b>
    </p>
<p>less will tell you if you enabled it correctly.</p>

![image](1photo/confirm.png)

<h3>Example 1:</h3>
Commands run:
<code>less -i ch1.txt</code><br>
<code>/changes</code>

      
<h4>Output:</h4>
      
![image](1photo/changes.png)
      
<p>This opens the ch1.txt file and shows the text file with a second command line under.
This is where you type what you are looking for, and in this case I typed changes.</p>
<h3>Example 2:</h3>
Commands run:
<code>less -i ch1.txt</code><br>   
<code>/joeBiden </code>
      
<h4>Output:</h4>
      
![image](1photo/ina.png)
      
<p>This is a great example of what the less command returns when it cannot find something</p>


<h2><code>?</code>Allows you to search a file backwards</h2>
<p>Here is the syntax for the command:
  <code>less[filename] </code>
    Filename is the name of the file we want to view, and less will display what is inside. Then it allows you
  to input search parameters. You then will do this:
  <code>?< phrase ></code> This will search for the word or phrase but, will search the file backwards.
    </p>
<h3>Example 1:</h3>
Commands run:
<code>less ch1.txt</code>
<code>?Americans</code>
  
      
<h4>Output:</h4>
      
![image](1photo/b1.png)
      
<p>This allows us to search for pervious occurences of the word Americans</p>
<h3>Example 2:</h3>
Commands run:
      
<code> less -i ch4.txt </code>
<code>?days</code>
      
<h4>Output:</h4>
      
![image](1photo/b2.png)
      
<p>This essentially searches from the last displayed line, which ends in "object." in this case, to the start of the text file. Here
we found only 1 occurence of the word days</p>

<h2> The Finale: Using multiple options in a search</h2>
<p>The cool thing about less is it lets you enable multiple command line options at once. Once you open a file in a less, you then can
  enable all the search options you want.</p>
  
<h3>Example 1:</h3>
<p> In this case we want the line numbers to display, and we to do a backwards-case-insensitive search.</p>

First thing we do:
Here is the code I ran: <code>less -N ch1.txt</code>
here is the generalized code: <code>less -N < fileName > </code>
As explained about this shows the line numbers:
  ![photo](1photo/ex1.png)
Now we can enable the search options we want:
  For the ignore case, we type in the less window <code>-i</code>
![photo](1photo/ex2.png)<br>
Now lets search for something backwards:
![photo](1photo/ex3.png)
 <code>?tHrEe</code>
  <p>Sucess! It has found what we are looking for </p>
  

<h3>Example 2</h3>
<p>Our goal is to have a case-sensitive forward search without the numbers showing on the left side.</p>
Here is the command we run:
<code>less ch1.txt</code>
<code>-i</code>
<p>For the keen eyed of you, you realize that -i, is used to enable case sensitive search as well. The best way to think of it is a switch. You turn the light on and off using the same switch. That is the same case as -i. It will let you know what type of search is enabled. As shown below.</p>
![image](1photo/sen.png)
  <p>Now lets specifiy directionality of the search. To search forward we use <code>/(what we are looking for)</code>, and to search backwards we use<code>?(what we are looking for)</code>. Less makes it very simple to use. Here is an example of running both forward and backwards:</p>
  <h4>For the forward search:</h4>
<code>/three</code>
  
![image](1photo/forward.png)
  
<p>Keep a notice of the line it presents when we run it from the same place. This gave us line 39.</p>
  <h4>For the backwards search:</h4>
<code>?three</h3>
  
![image](1photo/back.png)
  
  <p>This gave us line 20 instead of 39, since it searches backwards for the closest occurence</p>
  

  
