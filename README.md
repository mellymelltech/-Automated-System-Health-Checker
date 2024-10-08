# 🖥️ Automated System Health Checker

A Python-based tool that monitors key system performance metrics such as CPU usage, memory consumption, disk space, and network connectivity, providing alerts via email or messaging services when thresholds are exceeded. Great for system administrators to ensure continuous performance and prevent downtime.

## 🚀 Features

- **🔍 CPU Monitoring**: Continuously checks CPU usage and notifies if it exceeds a specified limit.
- **💾 Memory and Disk Monitoring**: Tracks memory consumption and disk space, sending alerts when thresholds are crossed.
- **🌐 Network Connectivity Check**: Performs periodic ping tests to ensure network availability.
- **📧 Alert System**: Sends notifications via email or Slack when performance issues are detected.
- **🔄 Scheduled Tasks**: Run at regular intervals using cron jobs or task schedulers.

## 🛠️ Tech Stack

- **🐍 Python**: Core scripting language for monitoring and automation.
- **📡 SNMP**: For retrieving system performance data (optional).
- **📬 SMTP**: Email notification system.
- **🔧 Cron Jobs**: For automating periodic system checks.
- **📊 Matplotlib**: Generate reports/graphs for system usage (optional).

## ⚙️ Getting Started

### Prerequisites

- Python 3.x
- Email/Slack API credentials (for notifications)

### Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/system-health-checker.git
    cd system-health-checker
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Configure environment variables for email/Slack:
    ```bash
    export EMAIL_USER="your-email@example.com"
    export EMAIL_PASS="your-email-password"
    ```

4. (Optional) Set up a cron job to run the script periodically:
    ```bash
    crontab -e
    # Add the following line to run every hour
    0 * * * * /usr/bin/python3 /path-to-script/system_health.py
    ```

### Example Usage

Run the system checker:
```bash
python3 system_health.py

system-health-checker/
│
├── health_checker.py   # Core script for system monitoring
├── alerts.py           # Email and Slack alerting functionality
├── config.py           # Configuration and thresholds
├── requirements.txt    # Python dependencies
└── README.md           # Project documentation (this file)
