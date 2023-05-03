Download Link: https://assignmentchef.com/product/solved-cs31-project-3-grocery-cart-options
<br>
<span class="">In response to the emergence of the novel coronavirus, grocery stores have become very creative in enabling their customers to acquire groceries in many different ways that reduce potential virus exposure.  For example, the Ralph’s where I shop supports the following ways to fulfill grocery store orders:</span>







For this assignment, suppose that a sensor is recording grocery store order fulfillments at the sliding doors as they leave the store.  For example,

<span class="">    1P1D</span>

<span class="">would indicate that a single pickup and a single delivery order had been fulfilled.  From this information, note that the character P is being used to represent a pickup order, the character D is being used to represent a delivery order.  Similarly, the character S and I would represent shipped order and in-store order.  Additionally, lowercase letters p, d, s and i could also be used.  For example,</span>

<span class="">    5s10i</span>

<span class="">would indicate that five shipped orders and ten in-store orders had been fulfilled.  Additionally, no more than 20 pickup orders, no more than 10 delivery orders and no more than 99 total orders can be processed in one grocery store string.  For example,</span>

<span class="">    20p10d99i</span>

<span class="">would not be valid because more than 99 total orders are represented in this one grocery store string.</span>




<span class="">Precisely, to be a valid grocery store order string, </span>

<span class="">– digit(s) must be followed by an order type (p,d,s,i or P,D,S, I)</span><span class="">– leading extra zeros in the digit portion is not allowed</span>– only digit characters and the order type character are allowed.  No spaces or any other characters allowed– no more than 20 pickup type orders are allowed in a single grocery order string– no more than 10 delivery type orders are allowed in a single grocery order string– no more than 99 total orders are allowed in a single grocery order string

All of the following are examples of valid grocery store order strings:




<ul>

 <li><span class="">1p1d1s1i                            (a single pickup, single delivery, single shipped and single in-store order)</span></li>

 <li><span class="">5d5p                                 (five delivery and five pickup orders)</span></li>

 <li><span class="">1D1P4d4p                        (five delivery and five pickup orders)</span></li>

</ul>




<span class="">All of the following are examples of invalid grocery order strings:</span>




<ul>

 <li><span class="">happyDays10                        (no characters allowed besides digits, p, P, d, D, s, S, i or I)</span></li>

 <li><span class="">000001p                                (no leading zeros in the digit portion allowed)</span></li>

 <li><span class="">+1p                                          (no + allowed)</span></li>

 <li><span class="">1p1d   XYZ                             (string must be fully consumed to be valid)</span></li>

 <li><span class="">50i50i50s                              (no more than 99 orders total)</span></li>

 <li><span class="">10p10p10p1d1s1i                  (no more than 20 pickup orders allowed)</span></li>

 <li><span class="">5d5d5d1p1s1i                     (no more than 10 delivery orders allowed)</span></li>

</ul>




<h3><b><span class="">Your task</span></b></h3>




<span class="">For this project, you will implement the following five functions, using the exact function names, parameter types, and return types shown in this specification. (The parameter </span><span class=""><i>names</i> may be different if you wish).</span>

<b><code>bool isWellFormedGroceryOrderString(string grocerystring)</code></b>

<dl>

 <dd>

  <span class="">This function returns </span><span class="">true</span><span class=""> if its parameter is a well-formed grocery order string as described above, or  </span><span class="">false</span><span class=""> otherwise.</span>

 </dd>

 <dt>

  <code>int pickupCount(string grocerystring)</code>

 </dt>

 <dd>

  <span class="">If the parameter is a well-formed grocery order string, this function should return the number of pickup type grocery orders after the string is fully processed.  If the parameter is not a valid grocery order string, return -1</span><span class="">. </span>

 </dd>

 <dd>




 </dd>

 <dt>

  <code>int deliveryCount(string grocerystring)</code>

 </dt>

 <dd>

  <span class="">If the parameter is a well-formed <del>animal park</del> <u>grocery order</u> string, this function should return the number of delivery type grocery orders after the string is fully processed.  If the parameter is not a valid grocery order string, return </span><span class="">-1</span>.

 </dd>

 <dd>




 </dd>

 <dt>

  <code>int shipCount(string grocerystring)</code>

 </dt>

 <dd>

  <span class="">If the parameter is a well-formed <del>animal park</del> <u>grocery order</u> string, this function should return the number of shipped type grocery orders after the string is fully processed.  If the parameter is not a valid grocery order string, return</span> <span class="">-1</span>.

 </dd>

 <dd>




 </dd>

 <dt>

  <code>int inpersonCount(string grocerystring)</code>

 </dt>

 <dd>

  <span class="">If the parameter is a well-formed <del>animal park</del> <u>grocery order</u> string, this function should return the number of in-person type grocery orders after the string is fully processed.  If the parameter is not a valid grocery order string, return</span><span class=""> </span><span class="">-1</span><span class="">. </span>

 </dd>

</dl>




<dl>

 <dd>




 </dd>

 <dt>

  <span class="">These are the only five functions you are required to write. </span><span class="">Your solution may use functions in addition to these five if you wish. While we won’t test those additional functions separately, using them may help you structure your program more readably. Of course, to test them, you’ll want to write a main routine that calls your functions. During the course of developing your solution, you might change that main routine many times. As long as your main routine compiles correctly when you turn in your solution, it doesn’t matter what it does, since we will rename it to something harmless and never call it (because we will supply our own main routine to thoroughly test your functions).</span>

 </dt>

 <dt>

  <span class=""> </span>

 </dt>

 <dt>

  <span class="">Clearly, I am expecting the last four functions to invoke the first function as they complete their assigned task.  This code reuse is one of the major benefits of having functions.  So please do that.</span>

 </dt>

 <dt>

  <span class=""> </span>

 </dt>

 <dt>

  <span class="">Before you ask a question about this specification, see if it has already been addressed by the <a href="https://ccle.ucla.edu/mod/page/view.php?id=2992672">Project 3 FAQ</a>. And read the FAQ before you turn in this project, to be sure you didn’t misinterpret anything.  Be sure you also do the <a href="https://ccle.ucla.edu/mod/page/view.php?id=2992668">warmup exercises</a> accompanying this project.</span>

 </dt>

 <dt>

  <span class=""> </span>

 </dt>

 <dt>

  <span class="">Additionally, I have created a testing tool called CodeBoard to help you check your code.  CodeBoard enables you to be sure you are naming things correctly by running a small number of tests against your code.  Passing CodeBoard tests is not sufficient testing so please do additional testing yourself.  To access CodeBoard for Project 3, please click the link you see in this week named CodeBoard for Project 3.  Inside the file named user_functions.cpp, copy and paste your implementation of the assigned functions.  CodeBoard uses its own main( ) to run tests against your code.  Click Compile and Run.  However please be aware that no editing changes can be saved inside CodeBoard.  In this anonymous user configuration, CodeBoard is read-only and does not allow for saving changes.</span>

 </dt>

</dl>

<h3><b><span class="">Programming Guidelines</span></b></h3>

<span class="">The functions you write must not use any global variables whose values may be changed during execution (so global </span><em><span class="">constants </span></em><span class=""> are allowed).</span>

<span class="">When you turn in your solution, neither of the <del>four</del> <u>five</u> required functions, nor any functions they call, may read any input from </span><code><span class="">cin</span></code> <span class=""> or write any output to  </span><code><span class="">cout</span></code><span class="">. (Of course, during development, you may have them write whatever you like to help you debug.) If you want to print things out for debugging purposes, write to </span><code><span class="">cerr</span><span class=""> </span></code><span class=""> instead of </span><code><span class="">cout</span></code><span class="">. </span><code><span class="">cerr</span></code> <span class=""> is the standard error destination; items written to it by default go to the screen. When we test your program, we will cause everything written to </span><code><span class="">cerr</span></code> <span class=""> to be discarded instead — we will never see that output, so you may leave those debugging output statements in your program if you wish.</span>

<span class="">The correctness of your program must not depend on undefined program behavior. For example, you can assume nothing about </span><code><span class=""> </span><span class="">c</span></code><span class=""> </span><span class="">‘s value at the point indicated, nor even whether or not the program crashes:</span>

<pre>	int main()	{	    string s = "Hello";	    char c = s[5];   // c's value is undefined	    …</pre>

<span class="">Be sure that your program builds successfully, and try to ensure that your functions do something reasonable for at least a few test cases. That way, you can get some partial credit for a solution that does not meet the entire specification.</span>

<span class="">There are a number of ways you might write your main routine to test your functions. One way is to interactively accept test strings:</span>

<pre>int main()	{	    string s;</pre>

<pre>           cout.setf( ios::boolalpha ); // prints bool values as "true" or "false"</pre>

<pre>for(;;) { cout &lt;&lt; "Enter a possible grocery store string: "; getline(cin, s); if (s == "quit") break; cout &lt;&lt; "isWellFormedGroceryOrderString returns ";  cout &lt;&lt; isWellFormedGroceryOrderString(s) &lt;&lt; endl; cout &lt;&lt; "pickupCount(s) returns "; cout &lt;&lt; pickupCount(s) &lt;&lt; endl; cout &lt;&lt; "deliveryCount(s) returns "; cout &lt;&lt; deliveryCount(s) &lt;&lt; endl; cout &lt;&lt; "shipCount(s) returns "; cout &lt;&lt; shipCount(s) &lt;&lt; endl;  cout &lt;&lt; "inpersonCount(s) returns "; cout &lt;&lt; inpersonCount(s) &lt;&lt; endl;  }</pre>

<pre>            return 0;	}</pre>

<span class="">While this is flexible, you run the risk of not being able to reproduce all your test cases if you make a change to your code and want to test that you didn’t break anything that used to work.</span>

<span class="">Another way is to hard-code various tests and report which ones the program passes:</span>

<pre>	int main()	{	    if (!isWellFormedGroceryOrderString(""))		cout &lt;&lt; "Passed test 1: !isValidGroceryOrderString("")" &lt;&lt; endl;	    if (!isWellFormedGroceryOrderString("   "))		cout &lt;&lt; "Passed test 2: !isWellFormedGroceryOrderString("   ")" &lt;&lt; endl;	    …</pre>

<span class="">This can get rather tedious. Fortunately, the library has a facility to make this easier: </span><code><span class=""> </span><span class="">assert</span></code><span class=""> </span><span class="">. If you #include the header </span><code><span class="">&lt;cassert&gt;</span></code> <span class="">, you can call </span><code><span class="">assert</span></code><span class=""> </span><span class=""> in the following manner:</span>

<pre>	assert(<em>some boolean expression</em>);</pre>

<span class="">During execution, if the expression is true, nothing happens and execution continues normally; if it is false, a diagnostic message is written to </span><code><span class="">cerr</span></code><span class=""> telling you the text and location of the failed assertion, and the program is terminated. As an example, here’s a very incomplete set of tests:</span>

<pre>	#include &lt;cassert&gt;	#include &lt;iostream&gt;	#include &lt;string&gt;	using namespace std;	…	int main()	{	    assert( isWelLFormedGroceryOrderString("") == false );	    assert( isWellFormedGroceryOrderString("    ") == false );            assert( shipCount( "    " ) == -1 );            assert( deliveryCount( "      " ) == -1 );            assert( inpersonCount( "      " ) == -1 );            assert( pickupCount( "       " ) == -1 );</pre>

<pre>            assert( isWellFormedGroceryOrderString( "1s1d1i1p1S1D1I1P" ) == true );            assert( shipCount( "1s1d1i1p1S1D1I1P" ) == 2 );            assert( deliveryCount( "1s1d1i1p1S1D1I1P" ) == 2 );            assert( inpersonCount( "1s1d1i1p1S1D1I1P" ) == 2 );            assert( pickupCount( "1s1d1i1p1S1D1I1P" ) == 2 );	    …	    cerr &lt;&lt; "All tests succeeded" &lt;&lt; endl;            return 0;	}</pre>

<span class="">The reason for writing one line of output at the end is to ensure that you can distinguish the situation of all tests succeeding from the case where one function you’re testing silently crashes the program.</span>