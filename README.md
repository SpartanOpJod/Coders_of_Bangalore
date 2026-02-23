🚀 Coders of Bangalore

You ask Sam Altman for $2.2B in funding.
He laughs.
Then gives you 24 hours to prove you deserve it.

🧠 The Challenge

Collect raw Instagram data of all OpenAI followers and answer:

Who has the maximum posts?

Who has the maximum followers?

Who follows the maximum number of people?

How many page categories exist (Digital Creator, Non-Profit, etc.) and how many accounts belong to each?

No API.
No structured dataset.
Just raw scraped text.

Time limit: 24 hours.

📂 Project Structure
.
├── initial_data.txt   # Raw Instagram follower data
├── analysis.py        # Data parsing and analysis logic
└── README.md
🔍 Data Collection

Raw follower data was stored in initial_data.txt.

Each follower block contains:

username
no_of_posts
no_of_followers
no_of_following
name
type_of_page (optional)
bio (optional)

Since the data is unstructured text, it must be:

Split into chunks

Parsed line-by-line

Cleaned (remove commas, words like “posts”, “followers”, etc.)

Converted into usable numerical format

🧩 Data Parsing Logic

Each chunk is converted into a structured dictionary:

def parse_chunk(chunk): 
    chunk = chunk.strip()
    sep_chunk = chunk.split('\n')

    username = sep_chunk[0]
    no_of_posts = sep_chunk[1]
    no_of_followers = sep_chunk[2]
    no_of_following = sep_chunk[3]
    name = sep_chunk[4]

    if len(sep_chunk) > 5:
        type_of_page = sep_chunk[5]
        bio = "\n".join(sep_chunk[6:])
    else:
        type_of_page = "Unknown"
        bio = ""

    return {
        "username": username,
        "no_of_posts": no_of_posts,
        "no_of_followers": no_of_followers,
        "no_of_following": no_of_following,
        "name": name,
        "type_of_page": type_of_page,
        "bio": bio
    }

All chunks are stored in:

all_chunks = []
📊 Analysis Performed

Because Instagram formats numbers like:

1,946 posts

2 followers

1 following

We clean numeric values using regex before comparison.

🏆 1. Who Has Maximum Posts?

Extract numeric values

Compare across all users

Return the user with highest count

👑 2. Who Has Maximum Followers?

Same approach:

Remove non-numeric characters

Convert to integer

Track maximum

🔁 3. Who Follows Maximum People?

Clean "following" values

Identify highest count

🗂 4. Category Analysis

We collect unique page types:

categories = set()
for chunk in all_chunks:
    categories.add(chunk['type_of_page'])

Then compute:

Total unique categories

Distribution of accounts per category

🛠 Tech Stack

Python 3

Regex (re)

File I/O

Basic data parsing & cleaning

Set operations

⚠️ Challenges Faced

Unstructured raw text

Inconsistent number formatting

Missing category fields

Comma-separated values

Singular vs plural variations ("post" vs "posts")

💡 Key Learnings

Real-world data is messy

Data cleaning > algorithm complexity

Regex is extremely powerful for text normalization

Defensive coding prevents crashes

Parsing text into structured format is a critical skill in data engineering

⏱ Time Constraint

Completed under a 24-hour simulated deadline.

No external APIs were used.

🧠 If Sam Altman Asks Again…

Next version would include:

Pandas-based aggregation

Category frequency distribution

Visualization charts

Automated scraping pipeline

Error-resilient parser

🎯 Conclusion

From raw Instagram follower text to structured insights in 24 hours.

Challenge accepted.
Data cleaned.
Questions answered.

Now where’s the funding? 😌
