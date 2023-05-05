Download Link: https://assignmentchef.com/product/solved-csit121-csit821-object-oriented-design-and-programming-assignment-1
<br>
The scenario for this semester’s assignments is ‘big data’ or rather data analytics over shopping data. Each time a shop customer uses a point-card or similar, they are providing a rich history of their purchases to the shop which is then combined with customer information (which may be partially sources from elsewhere) to support marketing campaigns.

There are three assignments. All use this scenario. In the first assignment the focus is defining and testing the basic classes that will be needed. The focus of the second assignment is creating a GUI that supports user interaction. The focus of the third and final assignment is storage and analytics, that is, supports offline storage in text files and supports analytics over the data.

Each assignment has two levels: advanced (max mark is 6 out of 6) or standard (max mark is 4 out of 6). An advanced assignment must be ready to be marked at the start of week 4 (assignment 1), 8 (assignment 2) and 12 (assignment 3). While a standard assignment can be marked in week 4 or 5 (assignment 1), week 8 or 9 (assignment 2), and week 12 or 13 (assignment 3).

Advanced level assignments have additional requirements beyond the standard version.

<h1>The key classes</h1>

Card and Purchase

There are three kinds of cards: AnonCard, BasicCard and PremiumCard. There is one kind of Purchase. Both AnonCard and BasicCard are free, while a PremiumCard has a $25 sign-up fee. A customer can also make purchases with cash; in which case there are no points accumulated.

Each Card has:

<ul>

 <li>ID</li>

 <li>points (the number of shopping points earned)</li>

</ul>

A Basic Card and Premium Card also have:

<ul>

 <li>name</li>

 <li>email</li>

 <li>balance (total value of prior purchases)</li>

</ul>

Each card has a different rule for calculating points.

<ul>

 <li>AnonCard:    0% of a purchase</li>

 <li>BasicCard: 5% of a purchase (if balance &lt; 500) otherwise 2.0% of a purchase</li>

 <li>PremiumCard: 2.5% of a purchase (if the purchase amount &lt; 40 and balance &lt; 1000) otherwise 3.0% of a purchase.</li>

</ul>

A purchase has:

<ul>

 <li>reciept ID</li>

 <li>card ID (or null if the purchase was made with cash)</li>

 <li>time</li>

</ul>

<h2>– purchase details (defined next)</h2>

To preserve some privacy, this shop does not record the details of every item purchased but only the amount purchased in a number of categories.

<h1>Code outline</h1>

public class Assignment1

{

static private ArrayList&lt;Card&gt;    cards;    static private ArrayList&lt;Purchase&gt; purchases;

public static void main (…)

{

// Test code goes here

}

public static void makePurchase ( … )

{

// …

}

}<strong> </strong>

<h1>Standard Level</h1>

<strong> </strong>

The purchase details are a hardcoded number of categories (up to 5). For example cat-A, cat-B, cat-C, cat-D and cat-E. Do not use these names, think of a shop, and create your own meaningful category names. The purchase details that need to be stored are: for each category the purchase amount.

One way to store a purchase (standard level) is:

<ul>

 <li>reciept ID</li>

 <li>card ID (or null of the purchase was made with cash)</li>

 <li>time</li>

 <li>cat_A amount</li>

 <li>cat_B amount</li>

 <li>cat_C amount</li>

 <li>cat_D amount</li>

 <li>cat_E amount</li>

</ul>

Note this may not be the best way.

Assignment 1 deliverables:

<ol>

 <li>Define the purchase class</li>

 <li>Test code that creates a list of purchases then prints the total shop purchase amount for each category 3. Define the card classes</li>

 <li>Test code that creates a list of cards (of mixed type) then prints (i) the total points earned by all customers and (ii) prints the number of customers with low (&lt; 500), medium (&gt;= 500 and &lt; 2000) and large (&gt;= 2000) points.</li>

 <li>Add a makePurchase method to your code. See the above outline. This method should have enough inputs to create a purchase object (including a Card ID or card object). This method creates a new purchase object based on the input details then adds this object into the purchase list.</li>

 <li>Test code that runs your makePurchase method several times.</li>

</ol>




Your solution will use the netbeans IDE. It will be console based. Your solution will make appropriate use of inheritance.

<h1>Advanced Level (CSIT821 students must complete this level)</h1>

<strong> </strong>

The advanced level includes all the requirements of the standard level plus the following features.




<ol start="5">

 <li>The purchase details are a flexible number of categories. For example cat-A, cat-B, cat-C, cat-D, cat-E, catF … Do not use these names, think of a shop, and create your own meaningful category names. The purchase details that need to be stored are: for each category the purchase amount. You will also need to store the category names somewhere.</li>

</ol>




<ol start="6">

 <li>The user can enter via the console an arbitrary number of thresholds (instead of the three required in standard deliverable number 4), then these thresholds will be used when reporting the number of customers in each of these point ‘bands’.</li>

</ol>




<ol start="7">

 <li>Reorganise your code so that there is an additional Shop class. The shop class has two attributes: (i) a list of cards and (ii) a list of purchases. The makePurchase method should be moved into the Shop class. New purchase obejcts should only be created in the Shop class. You’ll need to create a shop in your main method. Testing should then be done via various Shop class methods.</li>

</ol>


