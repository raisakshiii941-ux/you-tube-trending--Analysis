# 🎬 YouTube Trending Videos Analysis: What Makes a Video Go Viral?

A beginner-friendly data analysis project using Python, pandas, matplotlib, and seaborn to explore what patterns and habits help YouTube videos appear on the trending page.

---

## 📂 Dataset

**Name:** YouTube Trending Videos Dataset  
**Author:** The Devastator  
**Source:** [Kaggle — YouTube Trending Videos Dataset](https://www.kaggle.com/datasets/thedevastator/youtube-trending-videos-dataset)

Download `youtube.csv` from the link above and place it in the same folder as the notebook before running.

### Columns in the dataset

| Column | Description |
|--------|-------------|
| `video_id` | Unique ID for each video |
| `trending_date` | Date the video was trending (format: YY.DD.MM) |
| `title` | Video title |
| `channel_title` | YouTube channel name |
| `category_id` | Numeric category identifier |
| `publish_date` | Date and time the video was published |
| `time_frame` | Time of day the video was published (e.g. Morning, Evening) |
| `published_day_of_week` | Day of the week the video was published |
| `publish_country` | Country where the video was published |
| `tags` | Tags attached to the video |
| `views` | Total view count |
| `likes` | Total like count |
| `dislikes` | Total dislike count |
| `comment_count` | Number of comments |
| `comments_disabled` | Whether comments are turned off |
| `ratings_disabled` | Whether ratings are turned off |
| `video_error_or_removed` | Whether the video has an error or was removed |

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| **Python 3.10+** | Core programming language |
| **pandas** | Data loading, cleaning, and manipulation |
| **NumPy** | Numerical operations |
| **matplotlib** | Base charting library |
| **seaborn** | Statistical data visualisation |
| **Jupyter Notebook** | Interactive coding environment |
| **Google Colab** | Cloud-based Jupyter environment (recommended for beginners) |

---

## 🚀 Setup & Run Instructions

### Option A — Google Colab (recommended for beginners, no installation needed)

1. Go to [Google Colab](https://colab.research.google.com/)
2. Click **File → Upload notebook** and upload `youtube_analysis.ipynb`
3. In the **Files** panel on the left sidebar, click the upload icon and upload `youtube.csv`
4. Click **Runtime → Run all** to execute every cell from top to bottom
5. All charts and outputs will appear inline in the notebook

### Option B — Run locally on your computer

**Prerequisites:** Python 3.10 or higher must be installed.

```bash
# 1. Clone or download this project folder
# 2. Open a terminal in the project folder

# 3. (Optional but recommended) Create a virtual environment
python -m venv venv
venv\Scripts\activate        # Windows
# source venv/bin/activate   # macOS / Linux

# 4. Install all required libraries
pip install -r requirements.txt

# 5. Launch Jupyter Notebook
jupyter notebook

# 6. Open youtube_analysis.ipynb in the browser tab that opens
# 7. Make sure youtube.csv is in the same folder
# 8. Click Kernel → Restart & Run All
```

---

## 📊 Analysis Sections

The notebook is divided into 5 sections:

1. **Load & Explore Data** — load the CSV, check shape, data types, and preview rows
2. **Data Cleaning** — remove duplicates, fix date formats (`YY.DD.MM`), handle missing values, drop irrelevant columns
3. **Feature Engineering** — create `like_ratio` and `engagement_rate` columns
4. **Analysis & Visualisations** — 6 charts with insights:
   - Top 10 channels by total views
   - Average views per category
   - Best day of week to publish
   - Best time of day to publish
   - Likes vs views scatter plot + correlation heatmap
   - Effect of disabling comments on views
5. **Conclusions & Recommendations** — key findings and actionable tips for creators

---

## 🔑 Key Findings

1. **A few mega-channels dominate** — the top 10 channels (mostly music & entertainment) account for a disproportionate share of total trending views.
2. **Category matters enormously** — Music, Entertainment, and Sports categories consistently average far more views than niche topics.
3. **Mid-week publishing wins** — videos uploaded Tuesday–Thursday tend to gain more average views, likely due to higher weekday browsing habits.
4. **Afternoon/evening is prime time** — uploading between 2 PM and 8 PM increases early visibility because more users are actively on the platform.
5. **Likes, comments, and views are tightly linked** — a very high Pearson correlation (r ≈ 0.9+) shows that engagement and reach reinforce each other; ask viewers to like early!

---

## 📁 Project Structure

```
📦 youtube-analysis/
 ┣ 📓 youtube_analysis.ipynb   ← Main Jupyter Notebook
 ┣ 📄 requirements.txt         ← Python dependencies
 ┣ 📄 README.md                ← This file
 ┗ 📊 youtube.csv              ← Dataset (download from Kaggle separately)
```

---

## 📜 License

This project is for educational purposes only. The dataset is provided by The Devastator on Kaggle under their respective terms of use.
