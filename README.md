# Custom_RandomizedSearchCV README

Project Name: Custom RandomizedSearchCV Implementation - Building a custom metrics commonly used in machine learning similar to that of sklearn.metrics

# Table of Contents
1. Overview
2. Prerequisites
3. Project Structure
4. Data
5. Input
6. Model
6. Setup
7. Usage
8. Results
9. Contributing
10. License

# Overview

This project represents the author's endeavor to comprehend various metrics commonly employed in machine learning. The approach involves crafting custom code for each metric, similar to the implementation found in sklearn.metrics. The primary goal is to establish a solid understanding of the fundamental concepts, with no introduction of additional features. The focus remains strictly on the basics.

To achieve this, self-generated datasets have been employed. The project encompasses the development of code for essential metrics, including:

Confusion matrix
F1 score
Area under the curve
Accuracy score
Mean square error
MAPE (Mean Absolute Percentage Error)
R-squared error

The objective is to gain insight into these metrics through hands-on coding and practical application.

# Prerequisites

Python 3.6 or later preferably
Jupyter Notebook
Libraries listed in requirements.txt

# Project Structure

The project structure is organized as follows: \
├──data \
├── notebooks \
│─├── CountVectorizer.ipynb \
├── README.md \
├── requirements.txt \
└── LICENSE \

# Data
No external data has been used. This project contain 4 csv files, the description of the data is provided in the Input section. 
We employ a version-controlled approach to manage and track the data. This ensures data integrity and reproducibility throughout the project's lifecycle. We use the Data Version Control (DVC) program to maintain and version our datasets.

If you require access to the exact dataset used in Task 2, please send an email to [rathishsekhar@gmail.com](mailto:rathishsekhar@gmail.com). We will be happy to provide you with the necessary data and any additional information you may need.


# Input
The project involves working with four sets of self-generated data, each with the features explained below.

1. df_a:
    1. Shape: (10,100, 2)
    2. Columns: This data simulates the output of a classification model using two columns:
        1. Column 'Y': Represents the actual labels - Mono label, denoted by 1.
        2. Column 'proba': Represents the predicted probabilities, where values closer to 1 indicate positive predictions (1), and values closer to 0 indicate negative predictions (0). The number of positive points, as determined by the 'proba,' is significantly greater than the number of negative points, with a ratio of 100:1. Clearly, the dataset is heavily impabalanced
    3. The values are taken to have True Positives = 0, False Positives = 0, False negaitves = 100 and True Negatives = 10000 respectively. Thus df_a represents a toy dataset. 

2. df_b:
    1. Shape: (10,100, 2)
    2. Columns: Column names are similar to df_a, but unlike df_a, this data is representative to a real-dataset. This variation is introduced to observe how AUC and other metrics behave with different ranges of true positive and true negative values.
    3. The values are set to have a good mix of all of the confusion matrix parameters. 
    4. The data is constructed in a way that the 

3. df_c:
Shape: (2,853, 2)
We randomly generated the number of points. The number of positive points is slightly less than the number of negative points. Column 'Y' contains both labels, 1 and 0, and the respective probabilities are generated in the 'proba' column.
4. df_d:
Contains 157,201 (randomly generated) data points, representing data with real-valued features treated as 'Y' and 'Y_predicted.' This scenario assumes a regression-type model. The two columns are 'y' (assumed as the actual value) and 'pred' (assumed as the predicted value).
In summary, this project explores various scenarios with self-generated data to gain insights into different metrics and their behavior.


## Customization

One of the key features of this project is the ability for users to customize the dataset generation process. The user of this code is therefore encouraged to explore different sample sizes, feature dimensions, or class configurations,


# Model and Modules 
1. sklearn.metrics

# Setup

1. Clone this repository to your local machine:
git clone https://github.com/rathishsekhar/Custom_Performance_Metrics.git

2. Navigate to the project directory:
cd Custom_Performance_Metrics

3. Install the required Python packages:
pip install -r requirements.txt

# Usage

For exploring the tasks, refer to the jupyter notebook - notebooks/RandomizedSearchCV.ipynb

# Ethical Considerations
This project strictly adheres to ethical guidelines and practices:

1. **No User Data Used:** We want to emphasize that no user data has been used in the development or testing of this project. We are committed to safeguarding user privacy and ensuring that any data used is anonymized and ethically sourced.

2. **For Learning Purposes:** This project is created solely for educational purposes. Our primary goal is to provide a resource for learning and understanding the inner workings of RandomizedSearchCV. We encourage responsible and ethical use of this knowledge in real-world applications.

3. **Transparency:** We are dedicated to transparency in our project's goals and functionality. We encourage open discussion and feedback to ensure that our project aligns with ethical best practices.

We welcome collaboration and contributions from the community to help improve this project's ethical stance and effectiveness.

# Results
Using the custom code, we have successfully implemented functions that emulate the sklearn.metrics module.

1. Our implementation include:

    Developing custom code for the following metrics:
    Confusion matrix
    F1 score
    Area under the curve
    Accuracy score
    Mean square error
    MAPE (Mean Absolute Percentage Error)
    R-squared error
2. Implementing and obtaining visual representations of the ROC curve metrics.
3. We tested these functions with various datasets




# Maintainance and Updates

This project is a product of continuous learning and improvement. For now, there are no updates required howevever, your feedback, suggestions, and contributions are highly valued. If you have ideas, encounter issues, or want to collaborate, please don't hesitate to reach out. Together, we can continue to improve and refine this project.

# Contributions
Contributions to this project are welcome. To contribute:

Fork the repository.
Create a new branch for your feature: git checkout -b feature-name
Make your changes and commit them: git commit -m 'Add feature-name'
Push to your branch: git push origin feature-name
Create a pull request.

# License

This project is licensed under the MIT License. Feel free to use and modify the code as needed.
Feel free to adapt this README template to your specific data science project. It provides a clear structure and information for users and collaborators to understand and contribute to your project effectively