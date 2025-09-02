# 🌐 Web Traffic Analysis & Classification  

This repository contains two projects focused on analyzing and classifying web traffic logs:  

1. **User-Agent Traffic Classification** – Classify requests as **Good** or **Bad** traffic using ML models.  
2. **Web Traffic Log Analysis** – Extract inferences from raw server logs (requests, IPs, referrers, status codes, user-agents, geolocation, etc.).  

---

## 🎯 Objectives  

- Detect malicious/bad bots using **User-Agent string classification**.  
- Perform **deep exploratory analysis** of web traffic logs.  
- Derive insights like **requests per minute/hour, IP patterns, referrer sources, user-agent distribution, success/error rates, and geolocation trends**.  

---

## 📂 Projects  

### 🔹 1. User-Agent Traffic Classification  
- **Input:** Web traffic logs with `http_user_agent` field.  
- **Approach:**  
  - Label data using known bad/good bot keywords.  
  - Train & compare multiple ML algorithms (e.g., Logistic Regression, Naive Bayes).  
  - Classify requests as **Good** or **Bad**.  
- **Outcome:** Detect bad bot traffic with ML-driven classification.  

---

### 🔹 2. Web Traffic Log Analysis  
- **Input:** Log data with `timestamp`, `request`, `remote_addr`, `http_referrer`, `status`, `http_user_agent`.  
- **Key Inferences:**  
  - 📊 **Requests per Minute/Hour** → Average ~17 requests/minute, ~1078/hour.  
  - 🕵️ **IP Analysis** → Different IPs perform GET, POST, HEAD with varying distributions.  
  - 🌍 **Geolocation** → IPs mapped to Mumbai, India (The Constant Company, LLC).  
  - 🔗 **Referrer Analysis** → Majority traffic from `None`, followed by `prophaze.com`.  
  - 🖥️ **User-Agent Analysis** → Top devices: Windows NT 10.0, Linux, iPhone.  
  - 🌐 **Browser Analysis** → Top: AppleWebKit, Gecko, Googlebot, AhrefsBot, etc.  
  - ✅ **Status Codes** → ~94k successful vs ~35k unsuccessful requests.  
  - ⏰ **Temporal Patterns** → Peak traffic on `2023-08-11 04` (~22k requests), lowest during night hours.  

---

## 🛠️ Tech Stack  

- **Languages:** Python (Pandas, NumPy, Regex, Collections)  
- **Visualization:** Matplotlib, Seaborn  
- **ML Models:** Logistic Regression, Naive Bayes (extendable to others)  
- **Tools:** Google Colab, ipinfo.io API (for geolocation)  

---

## 🚀 Usage  

1. Clone this repo:  
```
   git clone https://github.com/yourusername/web-traffic-analysis.git
   cd web-traffic-analysis
```
2. Install dependencies:
```
pip install -r requirements.txt
```

3. Open the notebooks in **Google Colab** or run locally:

- `user_agent_classification.ipynb` → ML classification.

- `web_log_analysis.ipynb` → Exploratory data analysis & inferences.

## Example Outputs

- **Requests per Minute**: 17 avg/min

- **Top Referrer**: `None (Direct)`

- **Top Device**: Windows NT 10.0

- **Top Browser**: AppleWebKit

- **Peak Traffic**: Aug 11, 04:00 (~22k requests)

## Future Work

- Add **deep learning models** (e.g., LSTM for sequence analysis).

- Automate referrer categorization (organic, direct, paid).

- Build a **real-time dashboard** using Streamlit/Plotly.

- Extend geolocation mapping with **heatmaps.**

## Contributing

Contributions are welcome! Feel free to fork, improve, and raise PRs.
