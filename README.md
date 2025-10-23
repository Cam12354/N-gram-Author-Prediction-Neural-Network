# N-gram-Author-Prediction-Neural-Network
This project implements a neural network–based author attribution model — predicting the author of a given text sample using N-gram embeddings and feedforward neural networks. The model was designed and trained on classic literary works by five authors, then evaluated on unseen test sets. Although other authors should work, more testing will be done  

It consistently identifies the correct author in 95% of test cases on average, demonstrating strong text feature generalization and stylistic differentiation across authors.

🚀 Features

-Custom N-gram tokenizer for feature extraction

-Trainable embedding layer representing character-level patterns

-Fully-connected neural network for classification

⚙️Configurable hyperparameters:

-n (n-gram size)

-embedding_dim

-hidden_dim

-learning_rate

-num_iterations

⚙️ Usage
Run training and testing
python author_attribution.py

Optionally, you can specify the number of training iterations:

python author_attribution.py 7000

Example Output:

Coleridge -2142.7625 -3011.3940 -2190.0708 -3086.5576 -3611.0747 Best score index: 0
which is Coleridge

Eliot -2876.7627 -1644.8639 -3207.0559 -3330.0400 -4063.2598 Best score index: 1
which is Eliot

EBBrowning -2381.1250 -3575.1755 -1810.6450 -3862.8586 -3775.4502 Best score index: 2
which is EBBrowning

Emily Dickinson -1966.7783 -1710.0582 -1976.5044 -1469.4661 -2626.8359 Best score index: 3
which is Emily Dickinson

Shakespeare -3245.4607 -5002.3945 -2886.4644 -4750.6772 -1800.6693 Best score index: 4
which is Shakespeare

🧩 How It Works

Text Preprocessing:
Texts are tokenized into overlapping N-grams (e.g., 4-character chunks).

Embedding Layer:
Each N-gram is mapped into a dense vector space to capture stylistic nuances.

Neural Network:
A feedforward architecture learns to associate embedding patterns with specific authors.

Evaluation:
The trained model predicts the author for unseen text samples, and accuracy is reported out of 5 test cases.

📈 Example Parameters (Final Model)
Parameter	Value
N-gram size (n)	4
Embedding dimension (emb_dim)	64
Hidden layer size (hidden_dim)	256
Learning rate (lr)	0.003
Training iterations (num_iter)	5000
🧪 Results
Metric	Performance
Avg. Correct Predictions	5 / 5
Training Time	~45–60s (CPU)
Dataset Size	~5000 data points per author

Notably, stylistic overlap between E.B. Browning and S. Coleridge occasionally leads to misclassifications — an interesting insight into feature overlap in textual style.
