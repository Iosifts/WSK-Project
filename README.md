Purpose:
This code handles loading, preprocessing, training, and evaluating text data for binary classification using transformer models. It also provides prediction functionality for user-inputted text.

Workflow:
Data Loading and Preprocessing:

Load data from CSV and filter for relevant text and label columns.
Remove rows with NaN labels.
Split into train and test sets (80/20 split).
Convert labels to integer format (0 for "not relevant," 1 for "relevant").
Tokenization and Dataset Preparation:

Tokenize text data using model-specific tokenizers.
Format for PyTorch compatibility with input_ids, attention_mask, and labels.
Model Training and Evaluation:

Train with early stopping on transformer models (e.g., DistilBERT, BERT).
Evaluate using accuracy, F1, precision, and recall (macro-averaged).
Save best model checkpoints for evaluation.
Visualization:

Plot confusion matrix and ROC curve for model checkpoints.
Prediction CLI:

Load saved model and tokenizer to make real-time predictions on user-input text with probability outputs for "relevant" and "not relevant" classes.
Usage:
Run train_and_evaluate to train a model.
For evaluation, set checkpoint_path and model ID, then use evaluate_checkpoint.
For interactive predictions, execute main().
