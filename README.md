# PFDA

![Programming](https://rp2.center/wp-content/uploads/2023/03/evt2.jpg)
*Programming for Data Analytics* [[1]](#1)  

## About this repository

This repository contains the assignments and project completed for the module of Programming for Data Analytics in ATU with the lecturer Andrew Beatty. 
In order to complete the assignments some Python programming skills were used such as data manipulation with **Pandas**, data visualization with **Matplotlib**, and working with Jupyter Notebooks, along with basic file handling, string operations, and logic for simulations.

This README has been written with [Github's documentation on README](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes) and [Wenger's article on 'Why having a Readme on your internal project is essential'](https://wengerk.medium.com/why-having-a-readme-on-your-internal-project-is-essential-c85cb9dd8e65) in mind [[2]](#2) [[3]](#3).     
MarkDown was used in this README file and was based on [GitHub's Documentation](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax) [[4]](#4).

## Getting Started

This project processes and stores weather data using automation and scripting tools. Below is a guide to navigate the structure and use the files:

1. Navigate the Project  
Use [Computer Infrastructure](https://github.com/filipekojak88/computer_infrastructure/tree/main) to enter the project folder.

2. Run Automation  
Trigger workflows via [.github/workflows/weather-data.yml](.github/workflows/weather-data.yml) which runs [weather.sh](weather.sh). The `weather.sh` script downloads and saves Athenry's current weather data from the Met Éireann API with a timestamped filename.

Some background on `weather-data.yml` workflow:
- To automate the daily execution of the `weather.sh` script and push weather data to a GitHub repository, a GitHub Actions workflow was created. This involved adding a workflow file (`weather-data.yml`) to the `.github/workflows/` directory of the repository. The workflow is scheduled to run daily at 10 a.m. using the `cron` event and includes a `workflow_dispatch` event to allow manual testing. It uses a Linux-based Ubuntu virtual machine as the environment for running the actions.   
- The workflow clones the repository, executes the `weather.sh` script to fetch and save the weather data, and then commits and pushes the updated data back to the repository.    
- After creating and pushing the workflow file, the automation was tested by reviewing the logs in GitHub Actions to confirm the script executed correctly and new weather data was successfully committed to the repository. This was verified with the creation of [20241201_225405.json](data/weather/20241201_225405.json) and Commit message on GitHub [Update weather dta for 2024-12-01 22:54:07](https://github.com/filipekojak88/computer_infrastructure/commit/48b479227817f1ad66c57fcfbee927cea4b8365f).

3. Process Data 
- Timestamp files: Stored in [data/timestamps/](data/timestamps/).  
- Downloaded weather data: Check [data/weather/](data/weather/) for timestamped JSON files.

4. Analyze Weather Data  
Open [weather.ipynb](weather.ipynb) in Jupyter Notebook to explore and analyze the weather records.

Some background on `weather.ipynb` file:
- The file `weather.ipynb` documents a comprehensive process for weather data collection and analysis using Bash scripting and Python. It begins by outlining tasks such as creating directory structures, generating and formatting timestamps, and automating data downloads from Met Éireann’s API. Each task is meticulously detailed with commands like `mkdir`, `date`, and `wget`, explaining how to dynamically name and save weather data files with timestamps.
- The later sections cover creating and testing a Bash script (weather.sh) to automate data downloads, and a brief analysis of one of the collected weather data files. The analysis includes a short explanation of the dataset obtained from data.gov.ie, rounding out the report as a complete guide to data acquisition, management, and preliminary examination.

## Use of this project

This project serves as an example of how to automate data collection and analysis tasks using a combination of command-line tools, Bash scripting, Python, and GitHub Actions. In this project, users can learn practical skills for automating data pipelines, working with timestamps, and analyzing weather data programmatically.

Some suggested applications:

- Educational Value: It demonstrates how to structure a repository, use Linux commands, and create automated workflows with GitHub Actions. Students can adapt this project as a template for other automation tasks involving data collection and processing.
- Real-World Insights: By integrating weather data from Met Éireann, the project provides an example of how publicly available datasets can be used for meaningful analysis.

## Get Help

If questions are raised while checking this project, you can contact me via github, and I will be happy to provide more information. Full list of references is available at the end of this README file and the numbers provided across this README.md and the weather.ipynb files are direct links to their respective references in the reference section, which can provide further insights into the structure and fundamentals used to build this project.

## Contribute

This project reflects the author's understanding of data automation and analysis using Python and Bash scripting. Contributions and suggestions to improve the project are highly encouraged, as they can lead to more robust solutions and innovative features.
Additionally, the step-by-step nature of this project enables others to replicate the process or customize it to analyze datasets from different sources. The automation of daily data collection ensures consistency and demonstrates the practical use of continuous integration tools.

Contributions are welcome, especially those that improve functionality, enhance the readability of scripts, or add new features for analyzing weather data.

I used [openincolab.com](https://openincolab.com) to generate the following clickable link.      
It opens the [weather.ipynb](weather.ipynb) notebook in [Google Colab](https://colab.research.google.com)

<a target="_blank" href="https://colab.research.google.com/github/filipekojak88/computer_infrastructure/blob/main/weather.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

## Author

I am currently a Quality Engineer with a Production Engineering & Management background. Though I have had around 12 years of experience swinging between the medical device and car assembly industry, I am currently chasing a change in my career through this course of Data Analytics in ATU. My long term goal is to move into Artificial Intelligence. If you want to know more about me, please add me on LinkedIn: [Filipe Carvalho](https://www.linkedin.com/in/filipe-carvalho-8146232a/) 
  
  
# References:

<a id="1">[1]</a> 

<a id="2">[2]</a> About readmes (no date) GitHub Docs. Available at: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes (Accessed: 29 April 2024).   

<a id="3">[3]</a> Wenger, K. (2023) Why having a readme on your internal project is essential, Medium. Available at: https://wengerk.medium.com/why-having-a-readme-on-your-internal-project-is-essential-c85cb9dd8e65 (Accessed: 08 December 2024).       

<a id="4">[4]</a> Basic writing and formatting syntax (no date) GitHub Docs. Available at: https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax (Accessed: 29 April 2024).   

<a id="5">[5]</a>