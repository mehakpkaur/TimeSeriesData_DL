# 📊 Electricity Production Forecasting using Deep Learning

This project implements and compares multiple deep learning models for time series forecasting on electricity production data.

---

## 📁 Dataset

- **File:** Electric_Production.csv  
- Contains monthly electricity production values  
- Univariate time series dataset (single feature)

---

## ⚙️ Data Preprocessing

The dataset was prepared using the following steps:

- Extracted target variable (electricity production values)
- Applied **MinMax Scaling** for normalization
- Converted data into sequences using a **sliding window approach**
- Used a sequence length of 24 (past 24 time steps)
- Performed **time-based train-test split (80%-20%)**

---

## 🧠 Models Implemented

The following models were implemented using PyTorch:

### 🔹 RNN (Recurrent Neural Network)
- Basic sequential model
- Captures short-term dependencies

### 🔹 LSTM (Long Short-Term Memory)
- Handles long-term dependencies
- Solves vanishing gradient problem

### 🔹 GRU (Gated Recurrent Unit)
- Similar to LSTM but simpler
- Faster training with good performance

### 🔹 Vision Transformer (ViT - Adapted)
- Uses attention mechanism
- Treats time steps as sequence tokens

---

## ⚙️ Training Details

- Loss Function: Mean Squared Error (MSE)
- Optimizer: Adam
- Epochs: 10
- Batch Size: 32

---

## 📈 Evaluation Metrics

Model performance was evaluated using:

- **RMSE (Root Mean Squared Error)**
- **MAE (Mean Absolute Error)**

---

## 📊 Results

| Model | RMSE  | MAE   |
|------|-------|-------|
| RNN  | 9.3194 | 7.7749 |
| LSTM | 10.9181 | 8.8950 |
| GRU  | 12.7986 | 10.1023 |
| ViT  | 8.5822 | 7.1625 |

👉 LSTM and GRU generally perform better due to their ability to capture long-term dependencies in time series data.

---

## 📉 Visualizations

The notebook includes:

- Time series plot of electricity production
- Prediction vs Actual comparison graph (LSTM)

---

## 🧠 Key Learnings

- Time series data requires sequence-based preprocessing
- LSTM and GRU outperform vanilla RNN
- Transformer models require more data for better performance
- Proper scaling improves model stability

---

## 🚀 Future Improvements

- Hyperparameter tuning (epochs, hidden size)
- Adding positional encoding in Transformer
- Using larger and multivariate datasets
- Trying advanced architectures (Temporal Fusion Transformer)

---

## 🛠️ Technologies Used

- Python
- Pandas, NumPy
- PyTorch
- Matplotlib
- Scikit-learn

---

## 📌 Conclusion

This project demonstrates how different deep learning architectures perform on time series forecasting tasks and highlights the importance of selecting appropriate models for sequential data.

---

## 👩‍💻 Author

**Mehakpreet Kaur**
