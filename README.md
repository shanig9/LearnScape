# LearnScape
LearnScape provides personalized insights into student performance, highlighting strengths, weaknesses, and areas for improvement, creating a visual map of the learning journey.
# LearnScape: Personalized Learning Insights

**Description:**

LearnScape is a Python-based tool designed to provide personalized insights into student performance. By analyzing quiz data, LearnScape identifies key trends, highlights strengths and weaknesses with creative labels, and offers actionable recommendations for improved learning outcomes. It visualizes learning progress, empowering students and educators with data-driven insights to optimize learning strategies.

**Key Features:**

*   **Performance Analysis:** Analyzes student performance based on accuracy, quiz topics, difficulty levels, and time taken.
*   **Creative Insights:** Highlights strengths and weaknesses with engaging labels like "Areas of Expertise" and "Opportunities for Growth," providing a more personalized and motivating experience.
*   **Actionable Recommendations:** Suggests specific topics, question types, and difficulty levels for students to focus on to improve their learning.
*   **Visualizations:** Creates informative visualizations, including histograms of accuracy, box plots of performance by topic, scatter plots of time taken vs. accuracy, and count plots of difficulty and accuracy levels, and quiz submission hour of day.
*   **Flexible Data Handling:** Supports different ID column names and handles both string and numeric accuracy values.
*   **Robust Error Handling:** Includes comprehensive error handling to gracefully manage file errors, missing columns, and other potential issues.
*   **Two Dataset Support:** Can analyze user-specific performance data in comparison to a separate overall performance dataset.

**Getting Started:**

1.  **Prerequisites:**
    *   Python 3.x
    *   pandas (`pip install pandas`)
    *   matplotlib (`pip install matplotlib`)
    *   seaborn (`pip install seaborn`)
    *   scikit-learn (`pip install scikit-learn`) (If you want to use the ML part of the code)

2.  **Installation (Optional - if you make it a package):**
    ```bash
    pip install learnscape  # Or how ever you name your package
    ```

3.  **Usage:**

    1.  Prepare your data: You will need two CSV files:
        *   `user_data.csv`: Contains individual student quiz data with columns like ID, submission time, accuracy, quiz topic, difficulty, etc.
        *   `question_data.csv`: Contains information about the questions themselves, including topic, difficulty, and type.

    2.  Run the script:

        ```bash
        python your_script_name.py  # Replace your_script_name.py with the name of your Python file
        ```

    3.  Follow the prompts: The script will prompt you to enter the ID of the student you want to analyze or type 'exit' to quit.

4. **Example Data:**
    Provide example data in the repository so users can quickly test the code.

**Data Format (Example user_data.csv):**

```csv
id,submitted_at,quiz_created_at,accuracy,quiz_topic,quiz_difficulty_level,quiz_name
1,2024-10-27 10:00:00,2024-10-27 09:30:00,85%,"Mathematics","Medium","Math Quiz 1"
2,2024-10-27 11:00:00,2024-10-27 10:30:00,60,"Science","Easy","Science Quiz 1"
...
