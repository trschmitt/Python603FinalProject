# Netflix Viewing Data Analysis

This project analyzes Netflix viewing data to uncover trends in content consumption and user behavior. The analysis includes visualizations for viewing habits, most-watched titles, peak viewing times, and more. The insights are saved as image files for presentation purposes.

## Getting Your Netflix Data

Netflix allows you to request your own data for download. Follow these steps:

1. Navigate to Netflix’s [Get My Info](https://www.netflix.com/account/getmyinfo) page and request your data.
2. After sending the request, you will receive an email that you need to confirm.
3. After a short processing period (usually less than a day), you will receive another email with the download link.
4. Download the .zip file, which contains your viewing activity and other related data. The folder structure will resemble the following:
   - `ACCOUNT/`
   - `CONTENT_INTERACTION/ViewingActivity.csv`
   - `DEVICES/`
   - Other folders as applicable.

## Features

### 1. Data Cleaning and Preprocessing

- Converts the `Start Time` to a datetime format.
- Calculates `Duration (minutes)` from the provided duration.
- Filters out trailers and handles missing or incomplete data.
- Extracts features like year, month, day, hour, and day of the week for time-based analysis.
- Segments data into "Before Daughter" and "After Daughter" based on the birth milestone (July 27, 2022).

### 2. Analyses Included

#### a. **Most-Watched Titles**

- Analyzes top 10 most-watched movies and series for each profile.
- Graphs are saved as:
  - `most_watched_movies_<profile>.png`
  - `most_watched_series_<profile>.png`

#### b. **Viewing Habits**

- Compares viewing habits one year before and after July 27, 2022.
- Outputs a bar chart saved as `viewing_habits.png`.

#### c. **Peak Viewing Times**

- Creates a heatmap showing viewing activity by hour and day of the week.
- Graph saved as `peak_viewing_times.png`.

#### d. **Viewing Duration Distribution**

- Analyzes how long content is typically watched using a histogram.
- Graph saved as `viewing_duration_distribution.png`.

#### e. **Device Usage**

- Displays the top 10 most-used devices for watching Netflix.
- Graph saved as `device_usage.png`.

## How to Run

1. Place the ViewingActivity.csv `netflix-report/CONTENT_INTERACTION/ViewingActivity.csv` into the parent directory.
2. Open the included Jupyter Notebook (`netflix_analysis.ipynb`) in your preferred environment (e.g., Jupyter Lab, Jupyter Notebook).
3. Alternatively, run the script (`netflix_analysis.py`) in an IDE such as PyCharm.
4. Ensure all required Python libraries are installed:
   - `pandas`
   - `matplotlib`
   - `seaborn`
5. Follow the prompts and view the output graphs, which will be saved in the working directory.

## Libraries Used

- **Pandas**: For data manipulation and cleaning.
- **Matplotlib**: For creating visualizations.
- **Seaborn**: For enhanced visualization aesthetics.

## Customization

- Update the `movie_exceptions` list in the `classify_title` function to handle edge cases for movie titles.
- Modify graph aesthetics (e.g., color palettes) in the visualization functions.

## File Outputs

- **Graphs**:
  - `most_watched_movies_<profile>.png`
  - `most_watched_series_<profile>.png`
  - `viewing_habits.png`
  - `peak_viewing_times.png`
  - `viewing_duration_distribution.png`
  - `device_usage.png`
- **Cleaned Dataset**: `Netflix_ViewingActivity_Cleaned.csv`

## Future Improvements

- Explore correlations between viewing durations and peak times for deeper behavioral insights.
- Expand time analysis to seasonal or yearly trends.

## Bibliography

### Tools and Libraries
- **Pandas**: McKinney, W. (2010). Data Structures for Statistical Computing in Python. Proceedings of the 9th Python in Science Conference, 51–56. https://pandas.pydata.org/
- **Matplotlib**: Hunter, J. D. (2007). Matplotlib: A 2D Graphics Environment. Computing in Science & Engineering, 9(3), 90–95. https://matplotlib.org/
- **Seaborn**: Waskom, M. L. (2021). Seaborn: Statistical Data Visualization. Journal of Open Source Software, 6(60), 3021. https://seaborn.pydata.org/

### Data Source
- **Netflix Viewing Activity**: Retrieved using Netflix's "Get My Info" data request system. For more details, visit: [https://www.netflix.com/account/getmyinfo](https://www.netflix.com/account/getmyinfo)

### References
- Netflix Help Center: "Viewing Activity and History." [https://help.netflix.com/](https://help.netflix.com/)
- Python Documentation: [https://docs.python.org/3/](https://docs.python.org/3/)

## Acknowledgments

Thank you to Netflix for providing the viewing activity data, and a special thanks to the Python libraries that made this analysis possible.

