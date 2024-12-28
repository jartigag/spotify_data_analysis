# Spotify data analysis
Quarto notebook for analysing personal Spotify streaming data:

- Generates summaries of listening patterns over time, including top artists and tracks
- Creates heatmap visualizations showing listening frequency for top artists and tracks across different years
- Creates bar plots showing track start/end patterns and shuffle mode usage
- Compares listening habits with user library content

## Set up

You can use Spotify's [Download your data tool](https://www.spotify.com/us/account/privacy/) to request your account details and extended streaming history. After a few days, you'll receive a compressed JSON files by email. Simply decompress them and place them in the `input_files` directory.

## Data description
The streaming history contains a lot of data: Stream end time in UTC, platform used, play time, track details (name, artist, and album), podcast information (episodes and shows), unique identifiers such as track/episode URIs, and various playback details such as shuffle mode, skips, and offline status. You can find a better description of this data in Spotify's [Understanding my data](https://support.spotify.com/uk/article/understanding-my-data/) article.
