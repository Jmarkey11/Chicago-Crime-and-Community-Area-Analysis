# Chicago-Crime-and-Community-Area-Analysis

### Chicago Crime Arrest Prediction Project

### **Summary**
This project analyzes Chicago's 2012 crime data to predict whether a crime resulted in an arrest. The goal is to explore crime patterns and demonstrate the use of data science techniques, including database integration, data analysis, and machine learning, in a real-world context.

The workflow begins with SQL-based extraction of data from a relational database containing crime, census, GIS, health, and school datasets. Comprehensive preprocessing and feature engineering transform the raw data into a machine learning-ready format. Multiple machine learning models are implemented, and their predictions are aggregated through ensemble techniques to maximize accuracy and robustness.

This project not only highlights predictive modeling but also showcases skills in:
- Handling imbalanced datasets using bootstrap downsampling.
- Employing advanced evaluation techniques.
- Building ensemble models for enhanced predictive performance.

### **Methods Used**
1. **Data Preprocessing and Feature Engineering**:
   - **SQL Integration**: Extracted relevant features and records from a relational database using complex SQL queries.
   - **Data Cleaning**:
     - Removed or imputed missing values.
     - Standardized categorical and temporal features.
   - **Feature Engineering**:
     - Created new features, such as:
       - Temporal features: crime hour, day of the week, month.
       - Community area mappings.
     - Encoded categorical variables (e.g., primary crime type, community area).
   - **Class Balancing**:
     - Addressed imbalanced data by using bootstrap downsampling, creating multiple balanced datasets.

2. **Machine Learning Models**:
   - **Naive Bayes**: Simple probabilistic model leveraging feature independence assumptions.
   - **Logistic Regression**: Baseline linear classifier for binary outcomes.
   - **Random Forest**: Ensemble model leveraging decision trees to capture complex patterns.
   - **HDBSCAN**: Density-based clustering model applied to highlight spatial trends and clusters.
   - **MLP (Multi-Layer Perceptron)**: Neural network model for capturing non-linear relationships.

3. **Ensemble Predictions**:
   - **Majority Voting**: Aggregates predictions from multiple models to select the most common outcome.
   - **Weighted Ensemble with MLP**: Trains an additional perceptron layer to combine predictions using weighted probabilities.

4. **Evaluation Metrics**:
   - **F1 Score**: Measures balance between precision and recall.
   - **ROC AUC**: Evaluates classification performance across thresholds.
   - **Precision-Recall AUC**: Focuses on model performance for imbalanced datasets.
   - **Confusion Matrix**: Detailed analysis of true positives, false positives, true negatives, and false negatives.
   - **Classification Report**: Summary of precision, recall, and F1 scores for each class.

### **Technology and Libraries**
- **Programming Languages**: Python, SQL
- **Database**: SQLite
- **Libraries**:
  - **Data Manipulation and Visualization**: `pandas`, `numpy`, `matplotlib`, `seaborn`
  - **Machine Learning**: `scikit-learn`, `hdbscan`
  - **Deep Learning**: `torch` (for MLP model)
  - **Database Operations**: `sqlite3`
  - **Utility**: `tqdm`, `random`, `scipy`
Contributions and suggestions are welcome! 😊
