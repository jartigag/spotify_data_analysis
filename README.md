# Spotify data analysis

R Quarto notebook to analyse personal Spotify streaming data.
You can find an example of the report at: https://nataliaciria.com/spotify-stream-history-analyis/

## Set up

You can use Spotify's [Download your data tool](https://www.spotify.com/us/account/privacy/) to request your account details and extended streaming history.
After a few days, you'll receive the files by email.

This analysis uses [jsonlite](https://cran.r-project.org/web/packages/jsonlite/index.html) to convert raw JSON files to R dataframes, [dplyr](https://dplyr.tidyverse.org/) and [tidyr](https://tidyr.tidyverse.org/) for data manipulation, [lubridate](https://lubridate.tidyverse.org/) to handle dates and times, [knitr](https://yihui.org/knitr/) to display tables and [ggplot](https://ggplot2.tidyverse.org/) to create the graphs.
To export the graphs as SVG files for further editing in Adobe Illustrator or PowerPoint, you'll also need [svglite](https://www.tidyverse.org/blog/2021/02/svglite-2-0-0/).

```r
install.packages(c("jsonlite", "dplyr", "tidyr", "lubridate", "ggplot2", "svglite", "knitr"))
```

To generate an automatic report in RStudio, decompress the JSON files, place them in the `input_files` directory, open `spotify_data_analysis.Rproj` and `spotify_stream_analysis.qmd`, then click the "Render" button (if you're not familiar with Quarto rendering, check this [tutorial](https://quarto.org/docs/get-started/hello/rstudio.html#rendering)).

## Data description

The streaming history contains: Stream end time in UTC, platform used, play time, track details (name, artist, and album), podcast information (episodes and shows), unique identifiers such as track/episode URIs, and various playback details such as shuffle mode, skips, and offline status.
You can find a better description of this data in Spotify's [Understanding my data](https://support.spotify.com/uk/article/understanding-my-data/) article.
