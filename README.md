# 📚 Academic Journal Finder (Elsevier & Springer)

This repository provides tools to help researchers find suitable academic journals based on their research topics, using automatic web scraping for Elsevier and Springer.

## 🚀 Features
- 🔎 Search for journals using custom keywords or journal names
- 🏛️ Supports Elsevier and Springer platforms
- 📊 Retrieve impact factors, cite scores, acceptance times, journal types, and more
- 💾 Save all results locally into an SQLite database

## 📂 Repository Contents
- `Elsevier.ipynb` — Journal Finder for Elsevier
- `Springer.ipynb` — Journal Finder for Springer

## 📥 Input and 📤 Output Details

### Elsevier Journal Finder

**Input Required:**
- A list of **journal names** and **publication frequency**.
- You can edit the provided dictionary in the notebook.

Example:
```python
journal_data = {
  "Journal Name": ["Applied Energy", "Energy", "Renewable Energy"],
  "Frequency": [248, 204, 74]
}
```

**Output Generated:**
- Creates an SQLite database file named `elsevier.db`.
- Stores journal information including:
  - Journal name
  - Impact factor
  - CiteScore
  - Time to first decision
  - Time to acceptance
  - Acceptance rate
  - Journal type (Open Access, Subscription, Hybrid)
  - Direct journal link

---

### Springer Journal Finder

**Input Required:**
- A list of **keywords or phrases** related to your research field.
- You can edit the `keywords` list in the notebook.

Example:
```python
keywords = ["energy", "deep learning"]
```

**Output Generated:**
- Creates an SQLite database file named `springer.db`.
- Stores journal and paper information including:
  - Journal name
  - Journal link
  - Paper title
  - Paper link
  - Publication year
  - Publishing model
  - Impact factor
  - 5-year impact factor
  - Time to first decision
  - Number of downloads

## 🛠️ How to Run
1. Install the required Python packages:
   ```bash
   pip install pandas selenium beautifulsoup4 webdriver-manager
   ```
2. Open either `Elsevier.ipynb` or `Springer.ipynb` in Jupyter Notebook or JupyterLab.
3. Edit the input fields (`journal_data` or `keywords`) as needed.
4. Run the notebook cells step-by-step.
5. Wait for scraping to complete. Chrome browser will be controlled automatically.

## ⚠️ Disclaimer
This tool is intended for **personal academic use only**.  
It scrapes publicly available information to assist researchers in finding appropriate journals.  
The developer takes **no responsibility for misuse** or for any violations of publisher terms and conditions.  
Use this tool responsibly and comply with the rules of Elsevier and Springer platforms.

