<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Coders of Bangalore</title>
    <style>
        body {
            font-family: 'Segoe UI', sans-serif;
            background-color: #0f172a;
            color: #e2e8f0;
            margin: 0;
            padding: 0;
            line-height: 1.6;
        }

        .container {
            width: 85%;
            max-width: 1000px;
            margin: auto;
            padding: 40px 0;
        }

        h1 {
            font-size: 3em;
            color: #38bdf8;
            margin-bottom: 10px;
        }

        h2 {
            color: #facc15;
            margin-top: 40px;
        }

        h3 {
            color: #a78bfa;
        }

        p {
            margin: 10px 0;
        }

        ul {
            margin-left: 20px;
        }

        code {
            background-color: #1e293b;
            padding: 6px 10px;
            border-radius: 6px;
            display: inline-block;
            margin-top: 5px;
        }

        pre {
            background-color: #1e293b;
            padding: 15px;
            border-radius: 8px;
            overflow-x: auto;
        }

        .highlight {
            color: #22c55e;
            font-weight: bold;
        }

        .card {
            background-color: #1e293b;
            padding: 20px;
            border-radius: 10px;
            margin-top: 20px;
        }

        footer {
            margin-top: 50px;
            text-align: center;
            color: #94a3b8;
            font-size: 0.9em;
        }
    </style>
</head>
<body>

<div class="container">

    <h1>🚀 Coders of Bangalore</h1>

    <p>You ask for <span class="highlight">$2.2 Billion USD</span> in funding.</p>
    <p>He laughs.</p>
    <p>Then gives you 24 hours to prove you deserve it.</p>

    <div class="card">
        <h2>🧠 The Challenge</h2>
        <ul>
            <li>Collect raw Instagram data of OpenAI followers</li>
            <li>Find who has maximum posts</li>
            <li>Find who has maximum followers</li>
            <li>Find who follows the most people</li>
            <li>Count how many page categories exist</li>
        </ul>
        <p><strong>Deadline:</strong> 24 Hours</p>
    </div>

    <h2>📂 Data Collection</h2>
    <p>Raw data stored inside <code>initial_data.txt</code></p>

    <pre>
username
no_of_posts
no_of_followers
no_of_following
name
type_of_page (optional)
bio (optional)
    </pre>

    <h2>🧩 Parsing Strategy</h2>
    <p>Each user block is converted into a structured Python dictionary.</p>

    <pre>
{
    "username": username,
    "no_of_posts": no_of_posts,
    "no_of_followers": no_of_followers,
    "no_of_following": no_of_following,
    "name": name,
    "type_of_page": type_of_page,
    "bio": bio
}
    </pre>

    <h2>📊 Analysis Performed</h2>

    <div class="card">
        <h3>🏆 Maximum Posts</h3>
        <p>Clean numeric text → Convert to integer → Track maximum</p>
    </div>

    <div class="card">
        <h3>👑 Maximum Followers</h3>
        <p>Remove commas & words → Extract digits → Compare values</p>
    </div>

    <div class="card">
        <h3>🔁 Maximum Following</h3>
        <p>Normalize numbers → Identify highest value</p>
    </div>

    <div class="card">
        <h3>🗂 Category Count</h3>
        <p>Store unique page types using Python sets</p>
    </div>

    <h2>🛠 Tech Stack</h2>
    <ul>
        <li>Python 3</li>
        <li>Regular Expressions (re)</li>
        <li>File Handling</li>
        <li>Data Cleaning</li>
        <li>Set Operations</li>
    </ul>

    <h2>⚠️ Challenges Faced</h2>
    <ul>
        <li>Unstructured raw text</li>
        <li>Inconsistent formatting (1,946 posts vs 1 post)</li>
        <li>Missing category fields</li>
        <li>Singular vs plural formatting</li>
    </ul>

    <h2>💡 Key Learnings</h2>
    <ul>
        <li>Real-world data is messy</li>
        <li>Cleaning data is more important than algorithms</li>
        <li>Regex is powerful for normalization</li>
        <li>Defensive coding prevents crashes</li>
    </ul>

    <footer>
        <p>Challenge completed under simulated 24-hour deadline.</p>
        <p>Now… where’s the funding? 💸</p>
    </footer>

</div>

</body>
</html>