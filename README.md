# AB-Testing-for-Assessing-New-Web-Page-Impact-using-Python  

## 📝 __Overview__  
A/B Testing is a statistical method used to compare two versions of a product or service to determine which one performs better. It splits users randomly into two groups  * __Control Group__ sees the original version.  
* __Treatment Group__ sees the new version.
  
This project investigates whether a newly designed landing page improves conversion rates on an e-commerce site compared to the existing page. Python has been used to explore the dataset, perform statistical analysis, and apply an independent t-test to support business decisions regarding the page rollout.  

🧪 The independent t-test is applied as the primary inferential method, suitable for comparing means between two independent groups (control vs. treatment).
🧪 The dataset is sourced from Kaggle: Ecommerce AB Testing 2022 Dataset1 by putdejudomthai. (Link: https://www.kaggle.com/datasets/putdejudomthai/ecommerce-ab-testing-2022-dataset1)
🧪 All analyses and coding were conducted using Google Colab, a cloud-based Python environment that allows seamless integration with Google Drive and simplifies code execution and data handling. Jupyter Notebook could also be used as an alternative.  
  
💡 Other Use Cases for A/B Testing:
* Testing email subject lines for better open rates.  
* Comparing two app layouts to reduce user drop-off.  
* Measuring the impact of pricing strategies on sales.  
* Evaluating different call-to-action buttons for signup rates.  

## __📂 Contents__  
|    File Name     | File Type | Description |
|------------------|-----------|-------------|
|      README      |    MD     | Read this before anything else |
|      ab_data     |    CSV    | Dataset used for analysis |
| Code_AB_testing  |   IPYNB   | Python Notebook |
  
## __▶️ How to Execute the Program__
Before executing the program, download the CSV file `ab_data` and the IPYNB file `Code_AB_testing` from this repository. Afterwards, follow these steps:  
### If you are using Google Colab:  
•	Upload the downloaded files to a folder in your Google Drive.  
•	Open a browser and go to https://colab.research.google.com.  
•	Click on File > Upload Notebook.  
•	Select and open the downloaded IPYNB file.  
•	Click on the run button adjacent to each code snippet to run the code.  
### If you are using Jupyter Notebook:  
•	If you don’t have Anaconda or Jupyter Notebook installed, visit: https://www.anaconda.com and download the installer appropriate for your OS.  
•	After downloading, double-click on the downloaded file and follow the on-screen instructions to complete the installation process.  
•	Locate and run the program ‘Anaconda Prompt’.  
•	Run Jupyter Notebook after navigating to the folder containing the downloaded IPYNB file and the CSV file. For instance, if the files are located in a folder called PythonCode in Local Disk (D:), then you have to run _D:\PythonCode>jupyter notebook_.  
•	After opening the IPYNB file, select the code snippets and click on Run to run the code.  
  
## 🔍 __Observation__  
* The dataset includes ~294,000 users evenly split between control (old page) and treatment (new page) groups.  
* Conversion rates were 12.04% for control and 11.89% for treatment, showing minimal visual difference in the bar chart.  
* A two-sample t-test returned a p-value of 0.2156, which is greater than the 0.05 significance level—indicating no statistically significant difference between the two groups.  
* Required sample size per group was calculated to be 6,279, while the actual sample size exceeded 147,000 per group, ensuring adequate power.  
* Minimum Detectable Effect (MDE) was 0.10%, and Margin of Error was 0.0017, reflecting high precision in estimates.  
* The observed difference in conversion rates was -0.15%, suggesting the new page slightly underperformed.  
  
## 📌 __Things to Keep in Mind__  
* Significance level used: 5% (α = 0.05)  
* Ensure data integrity—no missing values in key columns.  
* MDE is a planning parameter and does not affect the actual observed result.  
* T-test assumes normality and equal variance, reasonable due to large sample size.  
* Modify the file path if you're reading the dataset from your own Drive in Colab.  
