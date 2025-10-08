This repo contains step-by-step pipeline to analyze the real estate ads in Almaty, Kazakhstan. The dataset was collected from [Krisha](https://www.krisha.kz/) (Kazakhstan’s largest real estate platform) and visualized using [Apache Superset](https://superset.apache.org/). 


![Dashboard Preview](https://github.com/user-attachments/assets/65fde8b7-f4d3-4a96-9d87-2273f5331ba6)

To install dependencies, run `pip install requests beautifulsoup4 lxml pandas tqdm` and `pip install geopy tqdm`.

##    Stack

 Python - data scraping and preprocessing

 BeautifulSoup, Pandas - web parsing and data cleaning

PostgreSQL - storage and queries

Apache Superset - interactive dashboard 

--------------------------------------------------------------------------------
## **Project Workflow**

1. Data Collection: scraped apartment listings from [krisha.kz](https://www.krisha.kz/) including titles, prices, locations, link, and apartment features (number of rooms and area in m2) 

2. Data Cleaning & Preparation: converted raw listings to structured CSV, parsed latitude and longitude, calculated `price_per_m2`, retrieved `district` via adresses 

3. Visualization in Superset using interactive dashboard with multiple chart types (see `/dashboard_apache_superset.jpg` for a snapshot) 


## **How to Reproduce** 


1. Clone the repository
   
    >git clone https://github.com/<your_username>/almaty-apartments-analytics.git
   
    >cd almaty-apartments-analytics
3. Load data into Superset (via Upload CSV to database)
4. Import the dashboard JSON (if provided)
5. Explore the visualizations interactively

## **Interactive Dashboard Import**

You can explore the interactive version of this dashboard directly in Apache Superset by importing the provided `dashboard_for_import.zip` file.
1. Open your Superset instance.

2. Navigate to Settings → Import Dashboards.

3. Upload `dashboard_for_import.zip`.

4. Superset will automatically create the charts, datasets, and layout. Then, you will see the “Almaty Apartments Analytics” dashboard in your list of dashboards. Note that you must have Superset version >= 2.0.




Feel free to contact me via [Telegram](https://t.me/a117sst) or email anel.salmenova@gmail.com.
