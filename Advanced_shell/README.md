# Advanced Shell Scripting: Automating Tasks with Pokémon API

## Project Overview
This project focuses on advanced shell scripting techniques to automate tasks, manage processes, and handle API requests. The goal is to interact with the [Pokémon API](https://pokeapi.co/) to retrieve, process, and summarize data about Pokémon, while implementing robust error handling, text manipulation, and parallel processing. The project is designed for novice learners to build practical skills in shell scripting for system administration and automation.

## Objectives
- Automate API requests to retrieve Pokémon data.
- Use advanced text manipulation tools (`jq`, `awk`, `sed`) to extract and format data.
- Implement batch processing and parallel data retrieval.
- Create summarized reports in CSV format.
- Add robust error handling and retry logic for API requests.
- Manage background processes for efficient data fetching.

## Prerequisites
- Basic knowledge of shell scripting (Bash).
- Familiarity with command-line tools like `curl`, `jq`, `awk`, and `sed`.
- Access to a Unix-like environment (Linux, macOS, or WSL on Windows).

## Tasks
1. **API Request Automation**  
   - File: `apiAutomation-0x00`  
   - Objective: Write a script to fetch Pikachu's data from the Pokémon API, save it to `data.json`, and log errors to `errors.txt`.

2. **Extract Pokémon Data**  
   - File: `data_extraction_automation-0x01`  
   - Objective: Extract Pikachu's name, height, weight, and type from `data.json` using `jq`, `awk`, or `sed`, and format the output.

3. **Batch Pokémon Data Retrieval**  
   - File: `batchProcessing-0x02`  
   - Objective: Fetch data for multiple Pokémon (Bulbasaur, Ivysaur, Venusaur, Charmander, Charmeleon) and save each to separate JSON files with a delay to handle rate limits.

4. **Summarize Pokémon Data**  
   - File: `summaryData-0x03`  
   - Objective: Generate a CSV report summarizing name, height, and weight for Pokémon from Task 2, and calculate averages using `awk`.

5. **Error Handling and Retry Logic**  
   - File: `batchProcessing-0x02`  
   - Objective: Enhance the batch processing script with error handling and a retry mechanism for failed API requests.

6. **Parallel Data Fetching**  
   - File: `batchProcessing-0x04`  
   - Objective: Fetch data for multiple Pokémon in parallel using background processes, ensuring proper process management.

## Directory Structure
```
Advanced_shell/
├── apiAutomation-0x00                         # Script for Task 0 (API request for Pikachu's data).
├── data_extraction_automation-0x01            # Script for Task 1 (extracting Pikachu's data).
├── batchProcessing-0x02                       # Script for Task 2 and Task 4 (batch retrieval with error handling and retry logic).
├── summaryData-0x03                           # Script for Task 3 (generating a CSV report and averages).
├── batchProcessing-0x04                       # Script for Task 5 (parallel data fetching).
├── data.json                                  # Output file for Pikachu's API data (Task 0).
├── errors.txt                                 # Log file for errors from API requests (Tasks 0, 2, 4, 5).
├── pokemon_data/                              # Directory to store individual Pokémon JSON files (Tasks 2, 4, 5).
│   ├── bulbasaur.json
│   ├── ivysaur.json
│   ├── venusaur.json
│   ├── charmander.json
│   └── charmeleon.json
├── pokemon_report.csv                        # CSV file containing the summarized Pokémon data (Task 3).
└── README.md                                 # This file
```
    
## Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/BunnyeNyash/ALXprodev-Devops.git
   cd ALXprodev-Devops/Advanced_shell
   ```
2. Ensure dependencies are installed:
   - `curl`: For making API requests.
   - `jq`: For parsing JSON data.
   - `awk` and `sed`: For text manipulation.
   Install on Ubuntu/Debian:
   ```bash
   sudo apt-get update
   sudo apt-get install curl jq
   ```
3. Create a directory for Pokémon JSON files:
   ```bash
   mkdir pokemon_data
   ```
4. Make scripts executable:
   ```bash
   chmod +x apiAutomation-0x00 data_extraction_automation-0x01 batchProcessing-0x02 summaryData-0x03 batchProcessing-0x04
   ```

## Usage
- Run each script as specified in the task instructions.
- Example for Task 0:
  ```bash
  ./apiAutomation-0x00
  jq . < data.json | head -n 50
  ```
- Check output files (`data.json`, `pokemon_data/*.json`, `pokemon_report.csv`) and error logs (`errors.txt`).

## Notes
- Ensure scripts handle errors gracefully (e.g., network issues, invalid API responses).

## Resources
- [Pokémon API Documentation](https://pokeapi.co/docs/v2)
- [Bash Scripting Guide](https://www.tldp.org/LDP/abs/html/)
- [jq Manual](https://stedolan.github.io/jq/manual/)
- [awk Tutorial](https://www.gnu.org/software/gawk/manual/gawk.html)
- [sed Tutorial](https://www.gnu.org/software/sed/manual/sed.html)
