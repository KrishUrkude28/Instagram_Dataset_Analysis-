#  Instagram Data Analysis

A comprehensive social media analytics project exploring Instagram engagement patterns, audience behavior, content performance, and hashtag ecosystems using a relational database structure.

The project combines data cleaning, SQL-style relational analysis, engagement metric engineering, temporal analysis, and audience segmentation to uncover actionable insights for content creators, brands, and digital marketers seeking sustainable Instagram growth.

---

##  Dataset Overview

The analysis is based on a relational Instagram database containing **7 interconnected tables** representing users, posts, engagement interactions, follower relationships, and hashtag networks.

### Database Schema

| Table      | Records | Description                                                               |
| ---------- | ------- | ------------------------------------------------------------------------- |
| Photos     | 257     | Post metadata including content type, filters, creator, and creation time |
| Users      | 100     | Creator profile information and account details                           |
| Likes      | 8,782   | User likes and reaction activity                                          |
| Comments   | 7,488   | Comment interactions and engagement data                                  |
| Follows    | 7,623   | Follower-followee relationships                                           |
| Tags       | 21      | Hashtag reference table                                                   |
| Photo_Tags | 501     | Mapping table connecting photos and hashtags                              |

---

##  Dataset Details

### Photos Table

Contains post-level information including:

* Photo ID
* Creator ID
* Image URL
* Content Type (`Photo`, `Video`, `Carousel`)
* Applied Filters
* Creation Timestamp

### Users Table

Stores creator profile attributes:

* Username
* Join Date
* Verification Status
* Privacy Settings
* Total Posts

### Likes Table

Tracks user engagement activity:

* User ID
* Photo ID
* Like Timestamp
* Follower Status
* Reaction Type

Examples:

* ❤️ Heart Emoji
* 👏 Clap
* 👍 Thumbs Up

### Comments Table

Captures audience interaction data:

* Comment Text
* Comment Timestamp
* Emoji Usage
* Hashtag Counts
* Commenter ID

### Follows Table

Maintains follower network information:

* Follower ID
* Followee ID
* Follow Date
* Activity Status

### Tags & Photo Tags

Provide hashtag metadata and photo-hashtag relationships for hashtag ecosystem analysis.

---

##  Data Processing

Several preprocessing operations were performed to prepare the dataset for analysis:

### Data Cleaning

* Removed duplicate records
* Standardized datetime formats
* Validated foreign-key relationships
* Cleaned hashtag labels
* Normalized reaction categories

### Datetime Engineering

Extracted temporal features including:

* Hour of Posting
* Day of Week
* Month
* Weekday vs Weekend Categories

### Engagement Metrics

Calculated custom engagement indicators:

* Total Engagement
* Engagement Rate
* Likes per Follower
* Comments per Follower
* Non-Follower Engagement Rate

---

## 📈 Key Analytical Findings

---

## 1️⃣ Content Performance Analysis

### The Static Image Advantage

Content type comparison revealed that traditional image posts continue to outperform other formats.

| Content Type | Average Engagement |
| ------------ | ------------------ |
| Photo        | **63.63**          |
| Video/Reel   | 63.08              |
| Carousel     | 62.54              |

### Key Insight

While videos and carousels remain competitive, standard image posts generate the highest overall engagement and engagement efficiency.

---

## 2️⃣ Filter Impact Analysis

### Authenticity Outperforms Heavy Editing

Comparison between filtered and unfiltered content revealed a slight advantage for natural imagery.

| Category         | Average Engagement |
| ---------------- | ------------------ |
| Unfiltered Posts | **63.50**          |
| Filtered Posts   | 63.15              |

### Business Implication

Audiences appear to respond more positively to authentic and natural-looking content compared to heavily stylized posts.

---

## 3️⃣ Posting Schedule Optimization

### Peak Engagement Hours

Analysis of hourly engagement patterns identified three major activity windows:

| Time     | Performance |
| -------- | ----------- |
| 9:00 AM  | High        |
| 12:00 PM | High        |
| 7:00 PM  | Highest     |

These periods represent optimal opportunities for maximizing audience visibility and interaction.

### Best Posting Days

| Day       | Average Engagement |
| --------- | ------------------ |
| Friday    | **74**             |
| Wednesday | **72**             |
| Sunday    | **55**             |

### Key Insight

Midweek and end-of-week content consistently outperforms weekend publishing.

---

## 4️⃣ Hashtag Ecosystem Analysis

### Organic Discovery Potential

A significant proportion of engagement originates from users who do not already follow the account.

| Metric             | Value     |
| ------------------ | --------- |
| Non-Follower Likes | **33.4%** |

This indicates strong hashtag-driven discovery and content reach beyond existing audiences.

---

### Most Frequently Used Hashtags

| Hashtag | Uses |
| ------- | ---- |
| #smile  | 59   |
| #beach  | 42   |

While these hashtags are popular, frequency alone does not guarantee performance.

---

### Highest Performing Hashtags

| Hashtag    | Average Engagement |
| ---------- | ------------------ |
| #delicious | **65.27**          |
| #beauty    | **65.15**          |

### Key Insight

Niche and context-specific hashtags generate stronger engagement than broadly used tags.

---

## 5️⃣ Audience Health Analysis

### Follower Activity Status

| Category          | Percentage |
| ----------------- | ---------- |
| Active Followers  | **55.1%**  |
| Dormant Followers | **44.9%**  |

### Business Implication

Nearly half of the audience is inactive, creating a substantial opportunity for re-engagement campaigns.

Potential strategies:

* Personalized content series
* Story interactions
* Polls and Q&A sessions
* Giveaways and contests

---

## 6️ Comment Sentiment & Community Engagement

### Emoji Usage Analysis

More than half of all comments contained emoji interactions.

| Metric               | Value      |
| -------------------- | ---------- |
| Emoji-Based Comments | **50.0%+** |

### Key Insight

Emoji reactions represent a major communication channel between creators and audiences.

Actively responding to these interactions can strengthen community engagement and increase audience loyalty.

---

##  Strategic Recommendations

### For Content Creators

* Prioritize high-quality photo content.
* Publish during peak engagement windows.
* Use niche hashtags alongside broad hashtags.
* Focus on authentic visuals rather than excessive filtering.
* Engage actively with comment sections.

### For Brands

* Schedule campaigns on Wednesdays and Fridays.
* Develop reactivation campaigns for dormant followers.
* Leverage hashtag communities for organic reach.
* Monitor engagement rate rather than follower count alone.

### For Social Media Managers

* Track non-follower engagement as a growth KPI.
* Optimize posting schedules using audience activity patterns.
* Build hashtag strategies around performance rather than popularity.

---

##  Technologies Used

* SQL
* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

##  Conclusion

This analysis demonstrates that Instagram growth is driven by a combination of content quality, strategic timing, hashtag optimization, and audience engagement. While photos remain the strongest-performing content type, authentic visuals, niche hashtags, and active community management provide the greatest opportunities for sustainable audience growth and organic discovery.
