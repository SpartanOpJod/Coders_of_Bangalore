<h1>🚀 Coders of Bangalore — Instagram Data Analysis with Pure Python</h1>
<p><strong>A raw Instagram data parsing & analytics project built using core Python in Jupyter Notebook</strong></p>

<hr>

<h2>🏙️ Project Story (Challenge Scenario)</h2>
<div class="box">
    <p>
        You ask for <strong>$2.2 Billion in funding</strong>.
        Instead, you receive a 24-hour data challenge.
    </p>
    <p>
        🎯 Goal:
        <ul>
            <li>Collect raw Instagram data of OpenAI followers</li>
            <li>Analyze engagement metrics</li>
            <li><span class="highlight">No APIs. No external libraries.</span></li>
        </ul>
    </p>
    <p>
        The only data provided: a raw text dump of Instagram profiles.
        Your job is to convert chaos into structured insights.
    </p>
</div>

<h2>🧠 What This Project Covers</h2>
<ul>
    <li>Raw text parsing</li>
    <li>Data cleaning & normalization</li>
    <li>Numeric extraction using Regex</li>
    <li>Profile metric comparison</li>
    <li>Category analysis</li>
    <li>Pure Python logic implementation</li>
</ul>

<h2>🛠️ Tech Stack</h2>
<ul>
    <li><strong>Language:</strong> Python 🐍</li>
    <li><strong>Environment:</strong> Jupyter Notebook</li>
    <li><strong>Libraries Used:</strong> re (built-in)</li>
    <li>❌ No pandas</li>
    <li>❌ No numpy</li>
    <li>❌ No external scraping APIs</li>
</ul>

<h2>📂 Project Structure</h2>
<pre>
Coders_of_Bangalore/
│
├── initial_data.txt
├── finaldata.txt
│
├── Data_Collection.ipynb
├── Final_Check.ipynb
├── Problem_Statement.ipynb
│
└── README.html
</pre>

<h2>📌 Phase 1: Initial Data Parsing</h2>
<p>
The project began with <code>initial_data.txt</code>.
Each Instagram profile was stored as a raw text block:
</p>

<pre>
username
no_of_posts
no_of_followers
no_of_following
name
type_of_page (optional)
bio (optional)
</pre>

<p>
Each block was converted into a structured Python dictionary.
</p>

<h3>Parsing Strategy</h3>
<ul>
    <li>Split text into chunks</li>
    <li>Extract fields line-by-line</li>
    <li>Handle optional category & bio fields</li>
    <li>Store all users in a list of dictionaries</li>
</ul>

<h2>📌 Phase 2: Final Data Integration</h2>
<p>
After validating logic on the initial dataset,
the cleaned parsing system was applied to <code>finaldata.txt</code>.
</p>

<ul>
    <li>Re-tested metric extraction</li>
    <li>Validated maximum comparisons</li>
    <li>Verified category distribution</li>
</ul>

<h2>📊 Core Analysis Tasks</h2>

<h3>🏆 Task 1: Who Has Maximum Posts?</h3>
<ul>
    <li>Remove commas & text ("posts")</li>
    <li>Extract numeric values</li>
    <li>Compare across all users</li>
</ul>

<h3>👑 Task 2: Who Has Maximum Followers?</h3>
<ul>
    <li>Normalize strings like "1,946 followers"</li>
    <li>Extract digits using Regex</li>
    <li>Identify highest follower count</li>
</ul>

<h3>🔁 Task 3: Who Follows Maximum People?</h3>
<ul>
    <li>Clean "following" values</li>
    <li>Convert to integers safely</li>
    <li>Track maximum</li>
</ul>

<h3>🗂 Task 4: Category Analysis</h3>
<ul>
    <li>Identify unique page categories</li>
    <li>Count how many accounts per category</li>
    <li>Handle missing categories safely</li>
</ul>

<h2>🧹 Data Challenges Identified</h2>
<ul>
    <li>Unstructured raw text blocks</li>
    <li>Inconsistent numeric formatting (1 post vs 1,946 posts)</li>
    <li>Singular vs plural word variations</li>
    <li>Missing category fields</li>
    <li>Non-uniform spacing</li>
</ul>

<h2>🧪 Why This Project Matters</h2>
<ul>
    <li>Simulates real-world messy data scenarios</li>
    <li>Strengthens data parsing fundamentals</li>
    <li>Demonstrates defensive programming</li>
    <li>Builds strong understanding of text normalization</li>
    <li>No shortcuts — pure logic implementation</li>
</ul>

<h2>🚀 Future Improvements</h2>
<ul>
    <li>Convert parsing logic into reusable modules</li>
    <li>Add visualization dashboards</li>
    <li>Automate scraping pipeline</li>
    <li>Optimize performance for large datasets</li>
</ul>

<footer>
    <p>
        <strong>Author:</strong> Aryan Srivastava <br>
        Computer Science Engineering Student — VIT Vellore <br>
        Building systems from raw data. Logic first. Tools later.
    </p>
</footer>