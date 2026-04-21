# Experiment_20

Aim - Perform a comprehensive data analysis on the global COVID-19 dataset.


Theory - Data analysis involves inspecting, cleansing, transforming, and modeling data to discover useful information and support decision-making. In this experiment, we perform Exploratory Data Analysis (EDA) on a global COVID-19 dataset.

Key concepts involved include:

	Data Wrangling: Converting raw data into a usable format (e.g., changing strings to datetime objects).

	Feature Engineering: Creating new metrics like 'Active Cases' from existing columns.

	Aggregation: Grouping data by geographical regions or time to see macro trends.

	Data Visualization: Using Choropleth maps and time-series plots to identify hotspots and growth rates.


Data Manipulation (Pandas)

	pd.read_csv(): Loads the external dataset from a CSV file into a DataFrame object.

	data.head(): Returns the first n rows (default 5) to provide a quick snapshot of the data structure.

	data.drop(columns, axis=1): Removes unnecessary columns (SNo, Last Update) to streamline the analysis.

	data.info(): Displays technical metadata, including non-null counts and data types for every column.

	astype(): Used to cast columns to specific types (e.g., converting 'ObservationDate' to datetime64 for time-series analysis).

	groupby(): A powerful tool used to split the data into groups (like Country/Region) and apply aggregate functions like sum() or max().

	reset_index(): Converts the index of a grouped object back into a standard DataFrame column, making it easier to plot.

	sort_values(): Reorders the data based on a specific column (e.g., sorting countries by the highest number of Confirmed cases).

	fillna(): Handles missing data by replacing NaN values with a specified string, such as "Unknown".


Data Visualization (Plotly Express)

	px.choropleth(): Creates a thematic map where geographic areas are colored in proportion to a statistical variable (Confirmed or Recovered cases).

	locationmode="country names": Automatically maps country strings to coordinates.

	color_continuous_scale: Defines the gradient (e.g., 'reds' for danger/confirmed, 'greens' for recovery).


Statistical Calculations

	Active Cases Formula: Confirmed - Deaths - Recovered. This derived metric represents the current burden on the healthcare system at any given time.


Conclusion - Through this experiment, we successfully processed a large-scale COVID-19 dataset to extract meaningful insights.
