# ML Music Recomender Project

A lightweight ML demo that predicts music preferences based on age and gender.

    •	Dataset: A small CSV file (music.csv) containing listener demographics (age, gender) and their associated music genres.
    •	Model: A Decision Tree Classifier built using scikit-learn, trained and tested in a Jupyter Notebook. An 80/20 train-test split is used, so accuracy may vary slightly between runs depending on the data split.
    •	Deployment: The trained model is saved using joblib, allowing fast predictions from new [age, gender] inputs without retraining.
    •	Visualization: The model’s decision logic is exported as a Graphviz .dot file, clearly displaying the tree structure and classification flow, with its simple “if-then” splits so anyone can trace the logic.

This project demonstrates a full ML pipeline—from preprocessing and modeling to saving and interpreting predictions—within a compact, beginner-friendly use case.
