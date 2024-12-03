# CyberSecurity_Analysis
VRV Security’s Python Intern Assignment

This repository contains a Python script designed to perform log analysis on Apache-style log files. It processes logs to gather useful insights such as request counts per IP address, the most accessed endpoint, and suspicious activity based on failed login attempts.

How to Use
Prerequisites:
Python 3.x
Required Python Libraries:
pandas (for data handling)
re (for pattern matching with regular expressions)
csv (for saving results to CSV files)
You can install the required libraries using:

bash
Copy code
pip install pandas
Steps to Run the Script:
Clone this Repository:

bash
Copy code
git clone https://github.com/your-repository-url.git
cd CyberSecurity_Analysis
Prepare Your Log File:

Place your Apache-style log file (logfile.log) in the same directory as the script, or update the log_file path in the script to point to your log file.
Run the Python Script: Execute the script using Python:

bash
Copy code
python log_analysis.py
This will:

Parse the log file.
Perform analysis to count requests per IP, find the most accessed endpoint, and detect suspicious activity (failed login attempts with status code 401).
Save the analysis results to a CSV file (log_analysis_results.csv).
Output:
The script will generate a CSV file log_analysis_results.csv with the following sections:

Requests per IP: Shows the number of requests made by each IP address.
Most Accessed Endpoint: Displays the endpoint with the highest number of requests.
Suspicious Activity: Lists IP addresses with more than 10 failed login attempts (401 status code).
Customizing the Regular Expression
By default, the script uses the following regular expression to parse Apache-style logs:

python
Copy code
log_pattern = r'(?P<ip>\S+) - - \[.*\] "(?P<method>\S+) (?P<path>\S+) \S+" (?P<status>\d+) .*'
This pattern captures:

ip: The IP address of the client
method: HTTP method (GET, POST, etc.)
path: Requested URL
status: HTTP status code
If your log format is different, you can modify this regular expression to match your log structure. For example:

If your log format includes a different structure or additional fields, you might need to adjust the pattern to capture those fields accordingly.
Make sure to test the regular expression before running the script with new log files to ensure it captures the necessary data.

Troubleshooting
Log Format Mismatch: If the script isn't parsing your logs correctly, review and adjust the log_pattern to suit your log format.
No Output CSV: If no results are written to the CSV file, ensure your log file contains data that matches the regular expression pattern and that it includes HTTP status codes (especially 401 for failed logins).