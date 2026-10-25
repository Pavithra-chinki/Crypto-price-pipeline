📈 Crypto Price Pipeline

A live cryptocurrency data pipeline that fetches real-time market data from the CoinGecko API, transforms it using Python and Pandas, and generates an automated market dashboard with visualisations.

🚀 What This Pipeline Does
Fetches live cryptocurrency data from CoinGecko API (no API key needed)
Transforms raw JSON response into a clean, structured DataFrame
Analyses market data — biggest gainers, losers, most expensive coins
Visualises price and 24h change data into a dashboard
Saves clean data to CSV with an automatic timestamp

📊 Sample Dashboard Output
Crypto Dashboard

💡 Key Insights Generated
Metric	Result
Coins Tracked	Top 10 by Market Cap
Most Expensive	Bitcoin ($80,609)
Biggest Gainer (24h)	Zcash (+6.87%)
Biggest Loser (24h)	TRON (-0.04%)
Data Currency	Live — fetched at runtime

🛠️ Tech Stack
Python 3.9
Pandas — data transformation and analysis
Requests — API calls to CoinGecko
Matplotlib — dashboard visualisation
CoinGecko API — free, no API key required

🔍 Pipeline Architecture
CoinGecko API
      ↓
  requests.get()        ← Fetch live JSON data
      ↓
  pd.DataFrame()        ← Transform to structured format
      ↓
  Analysis & Metrics    ← Biggest gainer, loser, most expensive
      ↓
  Matplotlib Charts     ← Price chart + 24h change chart
      ↓
  CSV Export            ← Timestamped output file
  
📁 Project Structure
crypto-price-pipeline/
│
├── crypto_pipeline.ipynb    # Main pipeline notebook
├── crypto_prices.csv        # Latest fetched data (auto-generated)
├── crypto_dashboard.png     # Dashboard visualisation
└── README.md                # Project documentation

🚀 How to Run
Clone this repository
bash
git clone https://github.com/Pavithra-chinki/Crypto-price-pipeline.git
Install dependencies
bash
pip install pandas requests matplotlib
Open the notebook
bash
jupyter notebook crypto_pipeline.ipynb
Run all cells — live data is fetched automatically every time you run it

🔄 What Makes This a Pipeline

Unlike a static analysis, this project:

Fetches fresh data every time it runs — no manual downloads
Timestamps every run automatically
Handles API responses and transforms JSON to structured data
Can be extended to run on a schedule (e.g. daily via Airflow or cron)

🔮 Future Enhancements
Schedule pipeline to run daily using Apache Airflow
Store historical data in BigQuery for trend analysis
Add email alerts when a coin moves more than 5% in 24h
Deploy to GCP Cloud Functions for serverless execution

👩‍💻 Author
Pavithra Sathia Kumar Data Engineer | GCP Professional Cloud Architect | Talend Certified
