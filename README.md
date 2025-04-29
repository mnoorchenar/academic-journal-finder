# 📚 Academic Journal Finder (Elsevier & Springer)

This repository contains two Jupyter notebooks to help researchers find suitable journals for their papers based on keywords.  
It automatically scrapes journal metadata from **Elsevier** and **Springer** platforms and saves it into SQLite databases.

---

## 🚀 Features
- 🔎 Search journals using custom keywords.
- 🏛️ Find journals from **Elsevier** and **Springer** databases.
- 📊 Retrieve impact factor, cite score, acceptance time, downloads, journal type, and more.
- 💾 Save all results locally into an SQLite database.

---

## 📂 Contents
- `Elsevier.ipynb` — Find journals and scrape metadata from Elsevier's Journal Finder.
- `Springer.ipynb` — Find journals and scrape metadata from Springer's search engine.

---

## 📥 Inputs
- **Elsevier**:  
  A manually prepared list of **journal names** with their **publication frequencies** inside the code (you can edit it).

- **Springer**:  
  A list of **search keywords** for building a search URL dynamically (you can edit the list).

---

## 📤 Outputs
- **Elsevier**:
  - An SQLite database file `elsevier.db`.
  - Contains journal name, impact factor, cite score, time to first decision, time to acceptance, acceptance rate, type (Open Access, Subscription, Hybrid), and journal link.

- **Springer**:
  - An SQLite database file `springer.db`.
  - Contains journal name, journal link, sample paper title, paper link, publication year, publishing model, journal impact factor, 5-year impact factor, time to first decision, and download counts.

---

## 🛠️ How to Use
1. **Install dependencies**:
   ```bash
   pip install pandas selenium beautifulsoup4 webdriver-manager
   ```

2. **Open** either `Elsevier.ipynb` or `Springer.ipynb` in Jupyter Notebook or JupyterLab.

3. **Modify inputs** if needed:
   - For Elsevier: Edit the `journal_data` dictionary (journal names and frequencies).
   - For Springer: Edit the `keywords` list (your research topics).

4. **Run** the notebook cells.
5. **Wait** while the tool automatically scrapes data and saves it into a database.

⚡ Chrome will open automatically during scraping; no manual browser control needed.

---

## ⚠️ Disclaimer
This tool is developed for **personal academic use only**.  
It scrapes publicly available information to assist researchers in finding appropriate journals.  
The developer takes **no responsibility for any misuse** or for any violation of third-party platform terms.  
Users are responsible for complying with the Elsevier and Springer platforms' terms and conditions.

