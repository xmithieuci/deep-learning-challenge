# Overview of the Analysis
The purpose of this analysis is to build a deep learning model that predicts the success of charity applications submitted to Alphabet Soup. Using historical data, the model aims to classify whether an application is likely to be funded (1) or not (0).

**Results**
**Data Preprocessing**
- Target Variable:
    - IS_SUCCESSFUL

- Feature Variables:
    - All other columns after encoding, including application type, affiliation, classification, use case, organization, income amount, special considerations, and ask amount.
- Removed Variables:

    - EIN: A unique identifier with no predictive value
    - NAME: Non-informative string column

**Compiling, Training, and Evaluating the Model**
- Model Structure:

    - Input Layer: Based on number of encoded features
    - Hidden Layer 1: 80 neurons, ReLU activation
    - Hidden Layer 2: 30 neurons, ReLU activation
    - Output Layer: 1 neuron, Sigmoid activation

- Model Performance:

    - Accuracy: ~72%
    - Loss function: Binary cross-entropy

- Steps Taken to Improve Performance:

    - Tuned neuron count and number of layers
    - Normalized data using StandardScaler
    - Consolidated rare categories into "Other"
    - Trained over 50 epochs

**Summary**
The final deep learning model achieved moderate accuracy (~72%), which falls slightly below ideal performance benchmarks. For better results, a tree-based algorithm such as Random Forest or XGBoost may be more effective for this structured dataset.