# Multilingual Expenses Tracker

## Overview
The **Multilingual Expenses Tracker** is a Python-based tool that helps you manage and track your personal expenses, view visualizations of your spending trends, and analyze your financial data across multiple languages. The tracker allows users to set a monthly budget, add expenses in different categories, and provides detailed expense statistics and visualizations. The tool also features multilingual support for Urdu, Arabic, and Hindi.

## Features
- **Multilingual Support**: Add and track expenses in multiple languages (English, Urdu, Arabic, Hindi).
- **Expense Categories**: Includes categories such as Food, Transport, Bills, Entertainment, Education/Stationary, Mobile Internet, Saving, and more.
- **Visualizations**: Generate pie charts, line charts, bar charts, and boxplots for expense distribution and trends.
- **Budget Tracking**: Set a monthly budget and track if you're exceeding it.
- **Expense Summary**: Get detailed statistics on your expenses, including total, average, median, and category-based breakdowns.

## Installation

To install the required dependencies, run the following commands:

```bash
!pip install gtts
!pip install playsound
!pip install gradio
!pip install transformers
!pip install torch
```

These libraries are used for text-to-speech, audio playback, user interface (Gradio), machine learning (Transformers and Torch), and data manipulation (Pandas, Matplotlib).

## Usage

1. **Set Your Budget**: Define your monthly budget in PKR.
2. **Add Expenses**: Add expenses in multiple categories. You can enter the expenses in different languages, and the app will automatically calculate and adjust your savings.
3. **View Visualizations**: Generate graphs that show your expense distribution and trends.
4. **Get Detailed Statistics**: View summary statistics such as total expenses, average expense, and category breakdown.

### Example Workflow

1. **Setting a Budget**:
   - Input your desired monthly budget.
   - The system will keep track of the total expenses and compare it with the budget.

2. **Adding Expenses**:
   - Enter the amount for each category (e.g., Food, Transport, etc.).
   - The system will automatically calculate the remaining budget and save any leftover amount as savings.

3. **Viewing Visualizations**:
   - Generate pie charts, line charts, bar charts, and boxplots to visualize your spending trends.

4. **Statistics**:
   - Get a detailed analysis of your spending with categories and monthly insights.

## Functions and Features

### `set_budget(budget)`
Sets the monthly budget in PKR.

### `add_expenses_multiple_categories(language, *amounts)`
Adds expenses for multiple categories, translates the status message into the selected language, and saves the expenses. If the budget is exceeded, an alert is triggered.

### `generate_comprehensive_visualizations()`
Generates visualizations like pie charts, line charts, bar charts, and boxplots based on the expenses data.

### `get_detailed_summary_statistics()`
Provides detailed statistics on total expenses, average expenses, category breakdowns, and monthly insights.

### `translate_text(text, target_lang)`
Translates the provided text into the desired language (Urdu, Arabic, Hindi).

## Gradio Interface

This project uses **Gradio** to build a web-based interface where users can interact with the tool:
- **Tabs** for setting a budget, adding expenses, visualizing data, and reviewing statistics.
- **Language Dropdown** for multilingual support.
- **Buttons** to add expenses, set budget, and generate visualizations.

To launch the interface, simply run the script, and the Gradio app will be hosted on a local or public URL.

## Example of Running the Program

```python
if __name__ == "__main__":
    os.makedirs('/content', exist_ok=True)
    tracker_interface = create_budget_tracker_interface()
    tracker_interface.launch(share=True)
```

This will launch the Gradio interface and make the app available on a public URL for use.

## Requirements

- Python 3.x
- `gtts`: Google Text-to-Speech for audio alerts.
- `gradio`: For building the user interface.
- `transformers` and `torch`: For language translation models.
- `pandas`: For data manipulation.
- `matplotlib` and `seaborn`: For data visualization.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
