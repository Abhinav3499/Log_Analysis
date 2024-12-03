# CyberSecurity_Analysis
VRV Security’s Python Intern Assignment

This repository contains a Jupyter Notebook designed for analyzing Apache-style log files. The notebook processes the logs to provide insights such as the number of requests per IP address, the most accessed endpoint, and suspicious activity based on failed login attempts (status code `401`). The analysis results are saved in a CSV file for easy review and further processing.

## How to Use

1. Clone the repository and navigate to the directory.
2. Place your Apache-style log file (`sample.log`) in the same directory as the notebook, or update the file path in the notebook.
3. Open the `Analysis.ipynb` notebook in Jupyter and run the cells sequentially.
4. The notebook will parse the log file, perform the analysis, and save the results in a CSV file (`log_analysis_results.csv`).

Feel free to customize the regular expression in the notebook if your log file format differs.
