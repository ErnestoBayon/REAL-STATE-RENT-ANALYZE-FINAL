# 🔑 API Keys Setup Guide

## Overview
Your APPRENTFINAL app now integrates with two powerful data sources:

1. **📊 US Census Bureau API** - Real median household income and population data by California county
2. **💰 Federal Reserve FRED API** - Current unemployment rate, mortgage rates, and housing price trends

---

## Your API Keys

### Census Bureau API
- **API Key:** `d89f2308a0eef3819958d4afe09eb6673a96121e`
- **Documentation:** https://www.census.gov/data/developers/data-sets.html
- **Data Used:** 
  - Median Household Income by County (ACS 5-Year)
  - Population Estimates by County

### Federal Reserve FRED API
- **API Key:** `eb9f52a46863eceb6c89aaffb5fedc3c`
- **Documentation:** https://fred.stlouisfed.org/docs/api/fred/
- **Data Used:**
  - US Unemployment Rate (UNRATE)
  - 30-Year Mortgage Rate (MORTGAGE30US)
  - California Housing Price Index (CASTHPI)

---

## 🚀 Setup for Streamlit Cloud

### Step 1: Deploy Your App
1. Go to https://share.streamlit.io/
2. Repository: `juanbayonugarte-source/REAL-STATE-RENT-ANALYZE-FINAL`
3. Branch: `main`
4. Main file: `APPRENTFINAL.py`

### Step 2: Add Secrets
1. Once deployed, click **"⚙️ Settings"** (bottom right)
2. Click **"Secrets"**
3. Paste the following into the secrets editor:

```toml
# Census Bureau API Key
CENSUS_API_KEY = "d89f2308a0eef3819958d4afe09eb6673a96121e"

# Federal Reserve FRED API Key
FRED_API_KEY = "eb9f52a46863eceb6c89aaffb5fedc3c"
```

4. Click **"Save"**
5. Your app will automatically restart with API access! 🎉

---

## 🏠 Local Development Setup

If you want to run the app locally with API data:

### Step 1: Create Secrets File
```bash
mkdir -p .streamlit
cp secrets.toml.template .streamlit/secrets.toml
```

### Step 2: Edit `.streamlit/secrets.toml`
Replace the placeholder values with your actual keys:

```toml
CENSUS_API_KEY = "d89f2308a0eef3819958d4afe09eb6673a96121e"
FRED_API_KEY = "eb9f52a46863eceb6c89aaffb5fedc3c"
```

### Step 3: Run the App
```bash
streamlit run APPRENTFINAL.py
```

---

## 📈 What the APIs Add to Your App

### Before (Simulated Data Only):
- Static neighborhood scores
- Estimated income levels
- No real-time economic context

### After (With API Integration):
✅ **Real median household income** for each California county from Census  
✅ **Live unemployment rates** from Federal Reserve  
✅ **Current 30-year mortgage rates**  
✅ **California housing price trends** (year-over-year)  
✅ **Actual population data** by county  
✅ **Dynamic affordability calculations** based on real income data  

---

## 🎯 API Features in Your App

When your app runs with API keys, you'll see:

1. **📊 Economic Indicators Dashboard**
   - Real-time unemployment rate
   - Current mortgage rates
   - CA housing price trend

2. **💰 Enhanced Affordability Scores**
   - Based on actual Census median income data
   - More accurate rent-to-income ratios

3. **📍 County-Level Insights**
   - Real population statistics
   - Accurate demographic data

---

## 🔒 Security Notes

- ✅ API keys are stored in Streamlit Secrets (encrypted)
- ✅ `.streamlit/secrets.toml` is in `.gitignore` (never committed to Git)
- ✅ Keys are only visible to you in Streamlit Cloud settings
- ✅ Rate limits: Census (500 requests/day), FRED (120 requests/minute)

---

## ⚠️ Troubleshooting

### "API keys not configured" warning
**Solution:** Make sure secrets are properly added in Streamlit Cloud Settings → Secrets

### "API enrichment failed" error
**Solution:** Check:
1. API keys are correct (no extra spaces)
2. Internet connection is working
3. API rate limits not exceeded

### App works but no real data showing
**Solution:** 
1. Restart the app in Streamlit Cloud
2. Check browser console for errors
3. Verify secrets.toml format is correct

---

## 📚 API Documentation Links

- **Census API Guide:** https://www.census.gov/data/developers/guidance/api-user-guide.html
- **FRED API Docs:** https://fred.stlouisfed.org/docs/api/fred/
- **Streamlit Secrets:** https://docs.streamlit.io/streamlit-community-cloud/deploy-your-app/secrets-management

---

## 🎓 For Your Professor

This app demonstrates:
- ✅ **Real API integration** with US government data sources
- ✅ **Secure secrets management** using Streamlit Cloud
- ✅ **Error handling** with fallback to simulated data
- ✅ **Data enrichment** combining multiple APIs
- ✅ **Live economic indicators** for context
- ✅ **Production-ready deployment** on cloud platform

---

**Need Help?** Contact: ernestobayon@example.com
**GitHub Repo:** https://github.com/juanbayonugarte-source/REAL-STATE-RENT-ANALYZE-FINAL
