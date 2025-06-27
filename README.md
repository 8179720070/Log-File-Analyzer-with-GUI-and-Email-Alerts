# 🔍 Log File Analyzer with GUI and Email Alerts

A Python-based desktop application that analyzes SSH and Apache log files, detects brute-force attempts and blacklisted IPs, generates visual reports, and optionally sends an email alert with a CSV report attached.

## 📌 Features

- ✅ GUI interface for ease of use (built with `tkinter`)
- 🔐 Detects brute-force attacks in SSH logs
- 🛑 Flags accesses from blacklisted IPs in Apache logs
- 📊 Visualizes top offending IPs using bar charts
- 📎 Exports incident report as a CSV file
- 📧 Optional email alert with attachment

---

## 🧰 Tools & Technologies

- **Python 3**
- `pandas` – for data handling  
- `matplotlib` – for plotting IP activity  
- `tkinter` – to build GUI  
- `smtplib` and `email` – to send emails  

---

## 🚀 Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/yourusername/log-file-analyzer.git
   cd log-file-analyzer
   ```

2. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

---

## 🖥️ How to Use

1. **Run the application:**

   ```bash
   python log_analyzer_gui.py
   ```

2. **Inside the GUI:**
   - Select SSH log file (e.g., `/var/log/auth.log`)
   - Select Apache log file (e.g., `/var/log/apache2/access.log`)
   - (Optional) Check the box to send an email alert
   - Click **"Run Analysis"**

3. **Output:**
   - Top IPs plotted as bar charts and saved as images
   - `output/incident_report.csv` generated
   - Email sent (if enabled)

---

## ⚙️ Configuration

Inside `log_analyzer_gui.py`, configure the following before using email:

```python
EMAIL_FROM = "youremail@example.com"
EMAIL_TO = "recipient@example.com"
SMTP_USER = "youremail@example.com"
SMTP_PASSWORD = "yourpassword"
BLACKLIST_IPS = ["103.27.202.91", "185.38.175.132"]
```

---

## 📂 Project Structure

```
├── log_analyzer_gui.py      # Main application script
├── requirements.txt         # Required Python libraries
├── output/                  # Stores generated CSV and charts
```

---

## 🙌 Acknowledgements
 Inspired by the need for simplified intrusion monitoring in small server environments.
