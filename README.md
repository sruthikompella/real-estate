Mini Real Estate Analysis Chatbot
Overview
This project is a Mini Real Estate Analysis Chatbot developed as part of a job assignment. The chatbot processes real estate data from an Excel file (Sample_data.xlsx) and responds to user queries with a summary, a chart, and a filtered data table. The Colab version uses Python with IPywidgets for a simple UI, while a separate React+Django implementation is available for a full web app experience.
Features

Query Processing: Handles queries like:
"Analyze Wakad" (provides a summary, price trend chart, and data table for Wakad).
"Compare Ambegaon Budruk and Aundh demand trends" (compares total units sold).
"Show price growth for Akurdi over last 3 years" (shows flat rate growth from 2022–2024).


Outputs:
A text summary (mocked LLM output).
A Plotly line chart for price or demand trends.
A filtered data table with downloadable CSV.


UI: A simple chat-style interface in Colab using IPywidgets (text input, submit button, and output area).

Technologies Used

Python: For data processing and visualization.
Pandas: For parsing and filtering Excel data.
Plotly: For interactive charts.
IPywidgets: For the Colab UI.
Google Colab: As the runtime environment.

Setup Instructions
Prerequisites

A Google Colab account (access via https://colab.research.google.com).
The Sample_data.xlsx file containing real estate data.

Steps to Run

Open Google Colab:

Go to https://colab.research.google.com and create a new notebook.


Upload the Excel File:

Click the folder icon on the left in Colab.
Click the upload button and select Sample_data.xlsx.
Alternatively, the script includes a simulated dataset for testing.


Install Dependencies:

The script automatically installs required libraries (pandas, openpyxl, plotly, ipywidgets) when run.


Copy the Script:

Copy the Python script from real_estate_chatbot_colab_ui.py (provided in the project files or assignment response) into a new code cell in Colab.
If using the actual Excel file, update the script to load the file by replacing the data dictionary with:df = pd.read_excel('Sample_data.xlsx')




Run the Script:

Run the cell to display the UI.
A text input box labeled "Query:" and a "Submit" button will appear.



Usage Guide

Enter a Query:

In the text box, enter a query such as:
"Analyze Wakad"
"Compare Ambegaon Budruk and Aundh demand trends"
"Show price growth for Akurdi over last 3 years"


The placeholder text provides examples of valid queries.


Submit the Query:

Click the "Submit" button to process the query.


View Results:

The output will appear below the input area, including:
Summary: A text summary of the analysis (e.g., "Analysis of Wakad: Over 5 years (2020-2024), the weighted average flat rate has shown growth, reaching 10,278 in 2024. Total units sold: 24,971.").
Interesting Fact: A highlight (e.g., "Interesting fact: Wakad saw its highest sales of 46.91B in 2022.").
Chart: A Plotly line chart showing price or demand trends (e.g., flat rate over years for Wakad).
Table: A filtered Pandas DataFrame (e.g., columns: year, total_sales - igr, total units, flat - weighted average rate).
Download: A filtered_data.csv file will be automatically downloaded.





Example Output for "Analyze Wakad"

Summary: "Analysis of Wakad: Over 5 years (2020-2024), the weighted average flat rate has shown growth, reaching 10,278 in 2024. Total units sold: 24,971."
Interesting Fact: "Interesting fact: Wakad saw its highest sales of 46.91B in 2022."
Chart: A line chart showing flat rates from 2020 (9,117) to 2024 (10,278) with data point labels.
Table:year  total_sales - igr  total units  flat - weighted average rate
2020  20.98B            3521         9,117
2021  30.26B            5262         9,289
2022  46.91B            6944         9,735
2023  38.81B            5484         9,960
2024  29.01B            3760         10,278



Project Structure

real_estate_chatbot_colab_ui.py: The main Python script for Colab, including the UI and logic.
Sample_data.xlsx: The input Excel file with real estate data (simulated in the script for demo purposes).
(Optional) real_estate_chatbot.html: A separate React+Django implementation for a full web app (not used in Colab but available for deployment).

Evaluation Criteria

Code Structure and Readability: The script is modular, with separate functions for data processing (process_query), display (display_results), and UI setup. Comments explain key steps.
Functional UI + Backend Integration: The IPywidgets UI provides a simple chat-style interface, and the backend logic processes queries accurately.
Correctness of Data Handling: The script correctly parses and filters the Excel data, including all years (2020–2024) for queries like "Analyze Wakad".
Visualization Clarity: The Plotly chart includes data labels and proper formatting for clarity.
Bonus: Includes the CSV download feature as an optional requirement.

Bonus Features (Optional)

LLM Integration: Not implemented in this version but can be added by connecting to the OpenAI API for real summaries.
Deployment: The Colab version is not deployed, but the React+Django version can be deployed on platforms like Vercel or Render. Instructions for this are in the original assignment response.

Limitations

Colab UI: The IPywidgets UI is basic compared to a full web app. For a more polished interface, deploy the React+Django version.
Interactivity: While the Plotly chart is interactive, the overall UI is limited by Colab's environment.
Excel File Loading: The script includes a simulated dataset. Ensure Sample_data.xlsx is uploaded to Colab for real data processing.

Future Improvements

Enhanced UI: Deploy the React+Django version for a modern web app experience with Tailwind CSS styling.
LLM Integration: Add OpenAI API for real-time summary generation.
More Query Types: Extend the chatbot to handle additional queries (e.g., "Show top areas by sales in 2023").

Submission Details

GitHub Repo: This project can be hosted in a GitHub repository with the Colab script, README, and the Excel file.
Live Demo: For a live demo, deploy the React+Django version on Vercel or Render (not applicable for Colab).
Video: A 1–2 minute video demonstrating the Colab UI and query processing can be recorded (optional).


