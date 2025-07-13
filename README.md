# AYTS - Autonomous Yield Trajectory Synthesizer

This project implements a deep learning-based time series synthesizer model named **Autonomous Yield Trajectory Synthesizer (AYTS)**. It learns from historical stock data (Open, High, Low, Close prices) and generates synthetic time series that closely resemble the real patterns.

---

## 📌 Features

- ✅ Google Colab + Google Drive integration
- ✅ Data preprocessing & normalization
- ✅ GRU-based encoder with neural regression head
- ✅ Synthetic time series generation
- ✅ Visual & statistical evaluation
- ✅ Metrics: MAE, MSE, RMSE, R², Kolmogorov–Smirnov test

---

## 🧠 Model Architecture

AYTS consists of two main components:

- **GRU Encoder**: Captures the temporal representation of sequential data.
- **Regressor**: A simple feed-forward neural network that generates the next predicted timestep.

Input Time Series (Sliding Window)
         ↓
     GRU Encoder
         ↓
   Feed-Forward Regressor
         ↓
  Next Time Step Prediction
📂 Dataset
The project uses historical stock price data in CSV format. Example: INCO.csv with the following columns:

Date, Open, High, Low, Close

Ensure your dataset is located in your Google Drive:

/content/drive/MyDrive/dataset/INCO.csv

🚀 How to Run
Upload the code in a Google Colab notebook or run it in your local environment.

Make sure your dataset is in the correct path.

Run the training, evaluation, and visualization cells.

🧾 Evaluation Metrics
After generating the synthetic data, we evaluate the quality by comparing it to the real data using the following metrics:

Feature	MAE	MSE	RMSE	R²	KS Statistic	KS P-Value
Open	...	...	...	...	...	...
High	...	...	...	...	...	...
Low	...	...	...	...	...	...
Close	...	...	...	...	...	...

📊 Visualizations
Line plot comparisons for each feature (original vs synthetic)

Pairplot distribution analysis using Seaborn

Training loss curve over epochs

<p align="center"> <img src="https://raw.githubusercontent.com/your-username/ayts-timeseries/main/assets/loss_plot_example.png" width="500"/> </p>
🔧 Dependencies
Install the required packages using pip:

pip install torch pandas matplotlib seaborn scikit-learn scipy

💡 Use Cases
Time series augmentation

Privacy-preserving data generation

Robustness testing for ML models

Financial market simulation

📜 License
This project is licensed under the MIT License. See the LICENSE file for details.

👤 Author
ranggaardhyy (boenyydev)
Email: ranggaardhyy22@gmail.com

🌐 Acknowledgments
PyTorch

scikit-learn

Seaborn

Google Colab

INCO Stock Dataset (Sample)
