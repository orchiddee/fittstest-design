# fittstest-design
This repository contains the source code for a customizable Fitts's Law experiment. It uses HTML to simulate target acquisition tasks, allowing for the collection of data on movement time as a function of target amplitude and width.

HOW TO RUN THE EXPERIMENT:

1. Get the Code
You have two easy ways to get this code onto your computer:

Download as ZIP (Easiest):

On this GitHub page, click the green < > Code button.
Select Download ZIP.
Unzip the downloaded file to a folder on your computer.
Clone with Git (for developers):
If you have Git installed, open your terminal or command prompt and run:
git clone https://github.com/orchiddee/fittstest-design.git

2. Open in Your Browser
Once you have the code on your computer:

Navigate to the folder where you unzipped or cloned the repository.
Find the file named fittstest.html.
Double-click fittstest.html. This will open the experiment directly in your default web browser (like Chrome, Firefox, Edge, etc.).
3. (Optional) Using a Live Server
If you're using Visual Studio Code (VS Code) and have the Live Server extension installed (highly recommended for web development), you can get a better development experience:

Open the project folder in VS Code.
Right-click on fittstest.html in the Explorer sidebar.
Select Open with Live Server.

EXPERIMENT EXPLANANTION:

Set Parameters: At the top of the page, you'll see input fields for Amplitude (A) and Width (W).

Amplitude (A): This is the distance the user has to move from the center of the start button to the center of the target button, measured in pixels.
Width (W): This is the diameter of the target button, measured in pixels.
As you change these values, the Index of Difficulty (ID) will update automatically below them. 
The ID is calculated using Shannon's formulation: ID=log2(A/W+1).
Prepare Experiment: Click the Prepare Experiment button. This will center the blue "Start" button in the experiment area.

Start a Trial: Click the blue Start button.

The "Start" button will disappear, and a red "Target" button will appear.
A timer begins as soon as you click "Start".
Complete the Trial: Quickly click the red Target button.

The timer stops the moment you click the target.
The Movement Time (MT) for that trial, along with the A, W, and ID values, will be recorded in the "Experiment Results" table below.
The "Start" button will reappear, ready for your next trial.
Repeat: You can repeat steps 3-4 as many times as you like with the same or different A and W values. Each successful trial will add a new row to the results table.

Download Results: Once you've collected enough data, click the Download Results as CSV button. This will download a .csv file (e.g., fitts_law_results.csv) containing all your recorded trials, which you can then open in spreadsheet software (like Excel, Google Sheets) for analysis.

DATA ANALYSIS AND PLOTTING (plotting.html)
This second HTML file provides a dedicated tool for analyzing the data collected from the Fitts's Law experiment (plotting.html). It allows you to upload the generated CSV file, visualize the relationship between Movement Time (MT) and Index of Difficulty (ID), and perform a linear regression to determine the Fitts's Law prediction equation and R-squared value.

This analysis tool helps you verify Fitts's Law, which states that Movement Time (MT) is a linear function of the Index of Difficulty (ID):

MT=a+b×ID

Where:

MT = Movement Time
ID = Index of Difficulty
a = Intercept (representing the inevitable delay or reaction time)
b = Slope (representing the information processing rate or constant of proportionality)

HOW TO USE THE ANALYSIS TOOLS:

Get the Code: Similar to the experiment page, you can either Download the ZIP of this repository or Clone with Git.
Open in Your Browser: Navigate to the folder and double-click the analysis.html file to open it in your web browser.
Upload Your Data:
Click the Choose File button and select the fitts_law_results.csv file that you downloaded from the Fitts's Law experiment page.
Analyze Data: Click the Analyze Data button.
The tool will process the CSV data, perform a linear regression, and display a scatter plot.
The plot will show your individual experiment data points (Movement Time vs. Index of Difficulty) along with a calculated regression line.
Below the chart, you'll see the calculated Prediction Equation (MT=a+b×ID) and the R-squared (R2) value. 
The R2 value indicates how well your data fits the linear model, with values closer to 1 suggesting a strong linear relationship.
