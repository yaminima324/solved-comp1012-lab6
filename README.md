Download Link: https://assignmentchef.com/product/solved-comp1012-lab6
<br>
<h2 id="question-1-password-checking">Question 1: Password checking</h2>

You are presented with a file <a href="passwords.txt" download=""><code>passwords.txt</code></a> where each line contains an email address followed by a password. The email address is separated from the password by a comma.

Your job is to write a Python script (starting with the template <code>lab6q1.py</code>) to flag all passwords that are not secure (or insecure).

A password is considered secure if it satisfies the following conditions:

<ul>

 <li>contains at least 8 characters,</li>

 <li>contains at least one numeric digit, and</li>

 <li>contains at least alphabet character.</li>

</ul>

Otherwise, a password is not secure.

Your Python script that will read in the file <code>passwords.txt</code> and for each insecure password, print the following information: * the line number in the file * the email address * the password * condition(s) password failed to be secure

At the end, you should also print the number of email addresses with insecure passwords.

For example, suppose the file <code>passwords.txt</code> contain the following lines:

<pre><code><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="2567404b0b694c655048444b4c514a47440b4644">[email protected]</a>,abc123<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="3f75505a117d5350487f465e575050115c5052">[email protected]</a>,ay799dkZ!<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="5d17323533730a32333a1d3a303c3431733e3230">[email protected]</a>,mrcool<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="5a08352d741c3f28343b343e351a32352e373b333674393537">[email protected]</a>,12345789<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="55063d303c3e3d7b1f2037343c27152038343b3c213a37347b3634">[email protected]</a>,ntyd888896<a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="682704011e0109462401280f05090104460b0705">[email protected]</a>,8739!</code></pre>

Then the output should look like:

<pre><code>Invalid Passwords Detail:1) <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="e3a1868dcdaf8aa3968e828d8a978c8182cd8082">[email protected]</a>,abc123:less than 8 characters3) <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="0a40656264245d65646d4a6d676b636624696567">[email protected]</a>,mrcool:less than 8 characters, no digit4) <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="e2b08d95cca487908c838c868da28a8d968f838b8ecc818d8f">[email protected]</a>,12345789:no alphabet character6) <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="aae5c6c3dcc3cb84e6c3eacdc7cbc3c684c9c5c7">[email protected]</a>,8739!:less than 8 characters, no alphabet characterThere were 4 emails with insecure passwords.</code></pre>

The file <code>lab5q1.py</code> contains two functions <code>hasNumbers(s)</code> and <code>hasAlpha(s)</code> which returns <code>True</code> if and only if <code>s</code> has a digit and alphabet character, respectively.

<h2 id="question-2-deduction-game">Question 2: Deduction Game</h2>

Write a game where a user has to guess a number from 1 – 99.

Your program will generate a random number <strong>once</strong> (pick a number), and will then prompts the user to repeatedly guess the number until they get it correct.

During the game, your program will test the number that the user entered compared to the number it picked. If the number that the user guessed is greater than the random number, tell the user “your guess is too low”. If the number that the user guessed is higher than the random number, tell the user, “your guess is too high”. Let the user continue guessing the number generated until they guess it right.

Once the user has successfully guessed the number, tell the user they win, and tell them how many guesses it took them to guess it right.

Use a loop to check your user input. Use string’s <a href="https://docs.python.org/3/library/stdtypes.html#str.isnumeric">.isnumeric()</a> to check to see if the user has provided you with a valid number before you use a cast to an integer. Your program <strong>should not</strong> crash if the user gives you bad input.

To create a random number use:

Sample game:

<pre>I've picked a number between 1 and 99, can you guess it? <mark>50</mark>Nope, it's not 50Your guess is too lowI've picked a number between 1 and 99, can you guess it? <mark>99</mark>Nope, it's not 99Your guess is too highI've picked a number between 1 and 99, can you guess it? <mark>42</mark>Nope, it's not 42Your guess is too lowI've picked a number between 1 and 99, can you guess it? <mark>93</mark>Nope, it's not 93Your guess is too highI've picked a number between 1 and 99, can you guess it? <mark>83</mark>You got it!It took you 5 guesses.</pre>

<h2 id="optional-new-and-improved-deduction-game">Optional: New and Improved Deduction Game</h2>

Once you’ve completed the guessing game, add some usability improvements. In the line that prompts the user for input, print the <em>known range</em> the random number could be in.

Do not increase the range if the user guesses outside your range. Example, if the current range is 40 to 60, do not change them if the user guesses 100.

Example:

<pre>Guess the number. 0 &lt; _ &lt; 100: <mark>50</mark>Guess the number. 0 &lt; _ &lt; 50: <mark>25</mark>Guess the number. 0 &lt; _ &lt; 25: <mark>12</mark>Guess the number. 12 &lt; _ &lt; 25: <mark>18</mark>Guess the number. 12 &lt; _ &lt; 18: <mark>14</mark>Guess the number. 14 &lt; _ &lt; 18: <mark>16</mark>Guess the number. 16 &lt; _ &lt; 18: <mark>17</mark>Congrats you guessed it in 7 tries</pre>

<strong>Challenge</strong>: What’s the fewest number of guesses you have to make for <strong>any</strong> range of numbers? <em>Hint</em>: This is a <em>search algorithm</em> called a <strong>binary search</strong>.

<span class="kksr-muted">Rate this product</span>