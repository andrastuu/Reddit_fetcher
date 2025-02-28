# Reddit Post Fetcher

## Description
This script fetches the latest posts from a specified subreddit using the Reddit API via the `praw` Python library. It includes anti-ban mechanics such as randomized user agents and request delays to avoid triggering rate limits.

## Features
- Authenticates with the Reddit API using credentials
- Fetches and displays the latest posts from a given subreddit.
- Implements automatic error handling and retries in case of API failures.
- Uses randomized user agents to minimize detection.
- Introduces delays between requests to reduce the risk of being rate-limited.

## Prerequisites
Ensure you have the following installed:
- Python 3.x
- `praw` library (`pip install praw`)
- `python-dotenv` for environment variable management (`pip install python-dotenv`)

## Setup
1. **Clone the repository**
   ```sh
   git clone https://github.com/your-repo/reddit-post-fetcher.git
   cd reddit-post-fetcher
   ```
2. **Input credentials**
   Change the CLIENT_ID and CLIENT_SECRET fields to your respective fields.
   You can set these up for free here: https://www.reddit.com/r/reddit.com/wiki/api/

2. **Run the script**
   ```sh
   python reddit_fetcher.py
   ```

## Usage
By default, the script fetches the latest 5 posts from `r/wallstreetbets`. You can modify the subreddit in the script or run it with a different subreddit name.

Example:
```python
fetch_latest_posts("technology", limit=10)
```

## Error Handling
- The script handles API request failures and automatically retries after a short delay.
- If authentication fails, an error message is displayed, and the script exits.

## Disclaimer
This script is intended for educational and personal use only. Scraping or interacting with Reddit must comply with [Reddit's API Terms of Service](https://www.reddit.com/wiki/api).

## License
MIT License

