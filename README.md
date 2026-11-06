# student-performance-decision-tree
Predicting student academic performance on the UCI dataset using a Decision Tree Classifier. Documents the progression from an overfitted baseline ($100\%$ train / $64.6\%$ test) to a depth-regularized model ($74.7\%$ test), highlighting the challenge of class imbalance and recall on failing students.

## Project Overview
* 🎯 **Problem:** Predict whether a student passes or fails final math grades without data leakage (dropping interim grades G1, G2, and G3).
* 🌲 **Baseline Model:** An unconstrained `DecisionTreeClassifier(random_state=42)` achieved 100% training accuracy and 64.6% test accuracy, demonstrating severe overfitting.
* ✂️ **Tuned Model:** Regularizing the tree with `max_depth=3` brought training (76.3%) and test (74.7%) performance into balance.
* ⚖️ **Key Insight:** Although overall accuracy improved, the model identified only 9 out of 27 failing students (33.3% recall), demonstrating why accuracy alone is insufficient when dealing with imbalanced classes.
