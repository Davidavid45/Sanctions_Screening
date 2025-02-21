# Sanctions Screening Tool

## Overview
This project automates the process of identifying publicly traded companies that appear on global sanctions lists. It integrates data from the Financial Modeling Prep (FMP) API for real-time stock data and the OpenSanctions API for sanctions screening. A local static dataset is also used for validation and additional cross-referencing.

## Features
- Retrieves real-time stock data from FMP API.
- Checks company symbols against global sanctions lists using OpenSanctions API.
- Processes and flags sanctioned entities through batch API requests.
- Cross-validates results with a static dataset.
- Outputs a structured report of flagged companies for compliance and risk analysis.

## Data Sources
- **Financial Modeling Prep API**: Provides publicly traded company symbols and real-time stock data.
- **OpenSanctions API**: Identifies entities subject to international sanctions.
- **Static Dataset**: Historical sanctions data for additional validation.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/sanctions-screening.git
   cd sanctions-screening
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Set up your API keys in a `.env` file:
   ```
   FMP_API_KEY=your_fmp_api_key
   SANCTIONS_API_KEY=your_sanctions_api_key
   ```

## Usage
Run the script to fetch stock data, check for sanctions, and generate a report:
```bash
python sanctions_screening.py
```

## Challenges and Considerations
- **API Rate Limits**: OpenSanctions API has a strict quota, requiring batch handling.
- **Data Standardization**: Mismatches in company names across sources required normalization.
- **Storage Issues**: Originally intended for Azure SQL Database, but connection issues necessitated alternative storage formats like CSV/JSON.

## Future Improvements
- Implement fuzzy matching for better company name recognition.
- Improve API rate handling with dynamic batching and retries.
- Develop a web interface for user-friendly data uploads and analysis.

## License
This project is licensed under the MIT License.

---
**Author:** Oluwasegun Adegoke
**GitHub:** [Your GitHub Profile](https://github.com/Davidavid45)

