# Automated Data Quality Analyst Agent

This project is an automated data quality analysis agent. It uses Python, pandas, and the Google Gemini API. The agent profiles a CSV file, generates visualizations, and uses a large language model to produce structured data cleaning recommendations.


---

## Table of Contents

-   [Features](#features)
-   [Getting Started](#getting-started)
    -   [Prerequisites](#prerequisites)
    -   [Installation](#installation)
-   [Usage](#usage)
-   [Project Overview](#project-overview)
-   [License](#license)

---

## Features

*   **Automated Data Profiling:** Calculates missing values, unique counts, and basic statistics for all columns.
*   **Visualization Generation:** Creates and saves histograms for numeric data and a missingness map visualization.
*   **AI-Powered Recommendations:** Uses the Gemini API to analyze data profiles and suggest remediation strategies.
*   **Structured Output:** Generates a JSON report including the data profile, AI recommendations, and paths to saved visuals.

---

## Getting Started

These instructions help set up the environment and run the data quality analysis notebook.

### Prerequisites

Python is required. The project uses several libraries and needs a Google AI API key.

*   Python 3.x
*   Required Python packages: `pandas`, `numpy`, `matplotlib`, `scikit-learn`, `google-genai`.

### Installation

1.  Clone the repository or download the script.
2.  Install the required Python packages:

    ```bash
    !pip install -q -U google-genai pandas matplotlib scikit-learn
    ```

3.  **Set up your API Key:** The script needs your Gemini API key as an environment variable named `GEMINI_API_KEY`. If running on platforms like Kaggle, use their secrets management.

    ```bash
    # Set this in your environment or secrets manager:
    export GEMINI_API_KEY="YOUR_API_KEY_HERE"
    ```

---

## Usage

The Python script is designed to run as a notebook or standalone script.

1.  **Prepare your data:** Ensure your main dataset is in CSV format. The script looks for a file named `sample_current.csv` in the current directory. You can optionally use a `sample_baseline.csv` for comparison.
2.  **Run the script:**

    ```bash
    python your_script_name.py
    ```

### Configuration Variables

You can adjust these variables in the script:

