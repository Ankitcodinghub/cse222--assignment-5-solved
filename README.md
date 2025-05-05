# cse222--assignment-5-solved
**TO GET THIS SOLUTION VISIT:** [CSE222 -Assignment #5 Solved](https://www.ankitcodinghub.com/product/cse222-assignment-5-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;95944&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;0&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;0&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;0\/5 - (0 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSE222 -Assignment #5 Solved&quot;,&quot;width&quot;:&quot;0&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 0px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            <span class="kksr-muted">Rate this product</span>
    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
&nbsp;

1 Introduction

In this assignment, you’re going to write a C program that uses recursion and dynamic programming to solve the egg drop analysis problem (EDAP). EDAP is a classic problem with a clever recursive solution whose e􏰃ective implementation requires dynamic programming.

2 Problem Statement

The Question

Given a number of identical eggs and a building with a number of 􏰇oors, one wishes to answer the question: what is the highest 􏰇oor from which an egg can be dropped without it breaking.

Approaches

There are many ways to do this:

<ul>
<li>given as many eggs as there are 􏰇oors, one can simply drop an egg from each 􏰇oor to discover the answer;</li>
<li>given only a single egg, one needs to start from 􏰇oor 1 and work towards higher 􏰇oors, since, once an egg is broken, it cannot be re-used</li>
<li>The cases in-between are more interesting. Given two eggs, one can try the middle 􏰇oor. If the egg survives, you only need to investigate the higher 􏰇oors (and you still have 2 eggs); whereas if the egg breaks, you need to investigate the lower 􏰇oors (and now only have one egg left).
The goal of EDAP is to determine worst case how many experiments must be run to answer The Question.

Note that you are not coming up with the algorithm for running these ex- periments (since the steps of the experiment depend on whether or not the egg survives any given drop).

1
</li>
</ul>
</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
3 Algorithm

You are to design and implement a function

<pre>int egg(int floors, int eggs);
</pre>
which will return the smallest number of experiments guaranteed to be su􏰅cient to answer The Question for the given number of 􏰇oors and eggs. One may de􏰄ne egg() recursively as follows:

0   1 

egg(f loors, eggs) = f loors 



min(1+max(egg(f −1,eggs−1),egg(floors−f,eggs))

1 ≤ f ≤ floors

This has the familiar repeated-subcase structure of other algorithms we’ve

been discussing (knapsack, rod cutting, etc.) and, similar to those, the per- formance is abysmal if coded as shown above. Therefore, you must employ dynamic programming to speed up the calculation of the egg function. You can do this by using a 500×500 array of ints:

<pre>int save[500][500]={0};
</pre>
where save[f][e] stores the value of eggs(f,e).

See your notes from lecture for various simplifying assumptions and other

relevant details.

4 Main Program

Your submission should include a main 􏰄le named 􏰁eggtest.c􏰂 and a make􏰄le for creating an executable 􏰄le named 􏰁eggtest􏰂 eggtest should simply:

1. ask the user for the number 􏰇oors;

2. ask for the number of eggs; and then

3. print the minimum guaranteed-su􏰅cient trials required, and exit.

Please don’t print anything else, ask for any other output, or perform any other actions. See /tmp/eggtest on the server for a sample executable.

5 Submission/Groups

<ul>
<li>You may work on this in groups of up to 3 people. If you do so, one person should submit via GitLab.</li>
<li>Submit via GitLab by creating a repository named 􏰁EggTest􏰂 and adding me as a reported by the due date (which is Monday, 9 March 2020 at 8:00 am).
2
</li>
</ul>
</div>
<div class="column">
floors ≤ 0 floors = 1 eggs = 1 otherwise

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
<ul>
<li>You must include a README 􏰄le (named 􏰁README􏰂) that indicates whether you worked on this alone or in a group, and, if you worked in a group, the full name of each group member (􏰄rst name + last name) as listed in Canvas</li>
<li>Include your source code, a make􏰄le, and the README 􏰄le only: no other 􏰄les please.</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
3

</div>
</div>
</div>
