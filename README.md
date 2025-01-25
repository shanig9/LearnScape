# LearnScape
LearnScape provides personalized insights into student performance, highlighting strengths, weaknesses, and areas for improvement, creating a visual map of the learning journey.

# LearnScape: Personalized Learning Insights

**Description:**

LearnScape is a Python-based tool designed to provide personalized insights into student performance. It analyzes quiz data, highlights strengths and weaknesses, and offers actionable recommendations.

**Key Features:**

*   Performance Analysis
*   Creative Insights
*   Actionable Recommendations
*   Visualizations
*   Flexible Data Handling
*   Robust Error Handling
*   Two Dataset Support
*   **Jupyter Notebook Compatibility:** Can be run directly in Jupyter Notebook or similar interactive Python environments.

**Getting Started:**

1.  **Prerequisites:**

    *   **Python 3.7+:** LearnScape is compatible with Python 3.7 and later versions. Check your version with `python --version` (or `python3 --version`).
    *   **Required Packages:** Install required packages using pip:

        ```bash
        pip install pandas matplotlib seaborn scikit-learn
        ```

2.  **Usage (Running from Source):**

    Since LearnScape is currently a set of Python scripts, you can run it directly from the source code.

    **Option 1: Running the main script:**

    1.  Place `main.py`, `analysis.py`, `recommendations.py`, `persona.py`, and `utils.py` in the same directory.
    2.  Prepare your data: Create `user_data.csv` and `question_data.csv` (see "Data Format" below).
    3.  Open a terminal in the directory containing the Python files and run:

        ```bash
        python main.py
        ```

    **Option 2: Running module directly:**
    1. Place `main.py`, `analysis.py`, `recommendations.py`, `persona.py`, and `utils.py` inside the `learnscape` directory and create `__init__.py` in the same directory.
    2. Prepare your data: Create `user_data.csv` and `question_data.csv` (see "Data Format" below).
    3. Open a terminal in the directory *containing* `learnscape` directory and run:

        ```bash
        python -m learnscape.analysis
        ```

    **Option 3: Running in Jupyter Notebook:**

    1.  Place all Python files (`main.py`, etc.) and your data files (`user_data.csv`, `question_data.csv`) in the same directory.
    2.  Open a new Jupyter Notebook in that directory.
    3.  Import the necessary functions and call them within the notebook cells. For example:

        ```python
        import pandas as pd
        from main import main #If you want to run the main function
        from analysis import generate_user_insights
        from recommendations import generate_user_recommendations
        from persona import analyze_student_persona

        user_df = pd.read_csv('user_data.csv')
        question_df = pd.read_csv('question_data.csv')

        # Example usage of analysis function
        insights = generate_user_insights(user_df, 1, 'id')
        print(insights)

        #Example to run main function
        main()
        ```

**Data Format:**

*   **user_data.csv:**

    ```csv
    id,submitted_at,quiz_created_at,accuracy,quiz_topic,quiz_difficulty_level,quiz_name
    1,2024-10-27 10:00:00,2024-10-27 09:30:00,85%,"Mathematics","Medium","Math Quiz 1"
    2,2024-10-27 11:00:00,2024-10-27 10:30:00,60,"Science","Easy","Science Quiz 1"
    ...
    ```

*   **question_data.csv:**

    ```csv
    question_id,question_difficulty_level,question_topic,question_type
    1,"Medium","Mathematics","Multiple Choice"
    2,"Easy","Science","True/False"
    ...
    ```

**Additional Notes:**

*   **File Organization:** For better organization, consider creating a `learnscape` directory and placing all `.py` files inside it (as described in the previous response about packaging). This is good practice even if you are not distributing it as a package.
*   **Error Handling:** The code includes robust error handling to catch common issues like missing files or incorrect data formats. Pay attention to the error messages if you encounter problems.
*   **Customization:** You can easily customize the analysis and recommendations by modifying the code in `analysis.py`, `recommendations.py`, and `persona.py`.
*   **Data Exploration:** Before using LearnScape, it's recommended to explore your data using pandas to understand its structure and identify any potential cleaning needs.

**Contributing:**

Contributions are welcome!

**License:**

[Choose a license]

**Contact:**

[Your Name/Email (Optional)]
