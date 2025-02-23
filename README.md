
# Predictors of Student Retention

## Project Overview
This project explores machine learning models to predict student retention outcomes. It utilizes a publicly available dataset on student performance, classifying students as **Graduates, Dropouts, or Enrolled**. The goal is to apply machine learning and deep learning models to optimize accuracy and generalization.

## Dataset Used
The dataset contains demographic, academic, and financial information on students. The target variable categorizes students into three classes: **Graduate (1), Dropout (0), and Enrolled (2)**.

## Model Performance Comparison Table

| Instance             | Optimizer Used | Regularizer Used | Epochs | Early Stopping | Number of Layers | Learning Rate | Accuracy | F1 Score | Recall | Precision |
|----------------------|----------------|------------------|--------|----------------|------------------|---------------|----------|----------|--------|-----------|
| Instance 1 (Basic NN) | Default        | None             | 50     | No             | 2                | Default       | 76.00%   | 0.69     | 0.69   | 0.75      |
| Instance 2 (Adam NN)  | Adam           | L1 & L2          | 100    | Yes            | 3                | 0.001         | 77.86%   | 0.71     | 0.70   | 0.76      |
| Instance 3 (RMSprop NN)| RMSprop        | L1 & L2          | 100    | Yes            | 3                | 0.001         | 78.61%   | 0.72     | 0.71   | 0.78      |
| Random Forest         | -              | -                | -      | -              | -                | -             | 77.71%   | 0.69     | 0.68   | 0.73      |

---

## Summary of Findings

- **Best Performance:** The **Optimized Neural Network with RMSprop (Instance 3)** achieved the highest accuracy at **78.61%**, benefiting from **L1 & L2 regularization**, **early stopping**, and an **optimized learning rate of 0.001**. It outperformed all other models.
- **RMSprop vs. Adam:** The **RMSprop optimizer** provided slightly better results in terms of **accuracy**, **precision**, and **recall** compared to the **Adam optimizer** (77.86%). This highlights the importance of choosing the right optimizer for deep learning models.
- **Traditional ML Algorithms:** **Random Forest** achieved **77.71% accuracy**, showing strong performance but still falling short compared to the optimized neural networks. Its strengths lie in simplicity and interpretability.
- **Impact of Regularization and Early Stopping:** Models with **L1 & L2 regularization** and **early stopping** showed better generalization, reducing overfitting and boosting performance on unseen data.

---

## Conclusion

The **Optimized Neural Network using RMSprop** emerged as the top performer, with **78.61% accuracy**. The combination of **regularization**, **early stopping**, and a **well-tuned learning rate** contributed to its success. On the other hand, the **Random Forest** model, with an accuracy of **77.71%**, remains a reliable, simpler alternative for this task.

The results confirm that deep learning models, when properly optimized, outperform traditional machine learning algorithms in terms of accuracy and generalization. However, **Random Forest** offers a good trade-off between performance and model complexity, making it a solid choice for similar tasks.

## Running the Project

1. Clone the repository:
   ```sh
   git clone https://github.com/Bfestus/Predictors-of-Student-Retention.git
   cd student-retention-prediction
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Run the Jupyter Notebook:
   ```sh
   jupyter notebook
   ```
4. Train models and evaluate performance.

---
### Author
Developed by **Festus Bigirimana**, Machine Learning Student at **African Leadership University** 🚀.
