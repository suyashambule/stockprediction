# LSTM Stock Price Prediction

This project implements a Long Short-Term Memory (LSTM) neural network to predict Apple Inc. (AAPL) stock prices using historical data. The model uses deep learning techniques to capture temporal patterns and make future price predictions.

## 🚀 Features

- **LSTM Neural Network**: Implements a 3-layer LSTM architecture for time series prediction
- **Data Preprocessing**: Includes data normalization using MinMaxScaler for optimal model performance
- **Interactive Jupyter Notebook**: Complete workflow from data loading to model training and evaluation
- **Historical Data Analysis**: Uses 5+ years of Apple stock data (2015-2020)
- **Visualization**: Comprehensive plots for data exploration and model performance analysis

## 📊 Dataset

The project uses Apple stock data (`AAPL.csv`) containing 1,258 records with the following features:
- **Date Range**: May 2015 to May 2020
- **Columns**: 
  - `symbol`: Stock symbol (AAPL)
  - `date`: Trading date
  - `close`, `open`, `high`, `low`: Stock prices
  - `volume`: Trading volume
  - `adjClose`, `adjHigh`, `adjLow`, `adjOpen`: Adjusted prices
  - `adjVolume`: Adjusted volume
  - `divCash`: Dividend cash
  - `splitFactor`: Stock split factor

## 🛠️ Technology Stack

- **Python 3.7+**
- **TensorFlow/Keras**: For building and training the LSTM model
- **pandas**: Data manipulation and analysis
- **NumPy**: Numerical computations
- **scikit-learn**: Data preprocessing (MinMaxScaler)
- **matplotlib**: Data visualization
- **Jupyter Notebook**: Interactive development environment

## 📋 Requirements

Install the required packages using:

```bash
pip install -r requirements.txt
```

## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone <your-repository-url>
cd stockprediction
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Launch Jupyter Notebook
```bash
jupyter notebook
```

### 4. Open the Main Notebook
Navigate to and open `LSTM.ipynb` in your browser.

### 5. Run the Cells
Execute the cells in order to:
- Load and explore the Apple stock data
- Visualize the closing price trends
- Preprocess the data (normalization and train/test split)
- Create sequences for LSTM input
- Build and train the LSTM model
- Make predictions and evaluate performance

## 🏗️ Model Architecture

The LSTM model consists of:
- **Input Layer**: Sequential data with 100 timesteps
- **LSTM Layer 1**: 50 units, return_sequences=True
- **LSTM Layer 2**: 50 units, return_sequences=True  
- **LSTM Layer 3**: 50 units
- **Dense Output Layer**: 1 unit (price prediction)

**Total Parameters**: ~50,851

## 📈 Model Training

- **Training Split**: 70% of the data
- **Test Split**: 30% of the data
- **Epochs**: 100
- **Batch Size**: 64
- **Optimizer**: Adam
- **Loss Function**: Mean Squared Error (MSE)
- **Sequence Length**: 100 timesteps

## 📊 Key Results

The model is trained to predict the next day's closing price based on the previous 100 days of closing price data. The notebook includes:
- Training and validation loss curves
- Predictions vs actual price comparisons
- Model performance metrics

## 📁 Project Structure

```
stockprediction/
├── LSTM.ipynb          # Main Jupyter notebook
├── AAPL.csv           # Apple stock historical data
├── requirements.txt   # Python dependencies
└── README.md         # Project documentation
```

## 🔄 Data Preprocessing Steps

1. **Data Loading**: Load CSV data into pandas DataFrame
2. **Feature Selection**: Extract closing prices for prediction
3. **Normalization**: Scale data to 0-1 range using MinMaxScaler
4. **Train/Test Split**: 70/30 split of the dataset
5. **Sequence Creation**: Generate input sequences of 100 timesteps
6. **Reshaping**: Format data for LSTM input (3D array)

## 📝 Usage Notes

- The model focuses specifically on closing price prediction
- Input sequences use 100 previous days to predict the next day
- Data is normalized to improve model convergence
- The notebook includes detailed comments explaining each step

## 🔮 Future Enhancements

- Incorporate additional features (volume, technical indicators)
- Implement multiple stock predictions
- Add real-time data fetching capabilities
- Experiment with different architectures (GRU, Transformer)
- Implement walk-forward validation
- Add more sophisticated evaluation metrics

## 🤝 Contributing

Feel free to fork this project and submit pull requests for improvements. Areas for contribution:
- Model architecture improvements
- Additional preprocessing techniques
- Enhanced visualization
- Performance optimization

## 📄 License

This project is available under the MIT License. See LICENSE file for details.

## ⚠️ Disclaimer

This project is for educational and research purposes only. Stock price predictions should not be used as the sole basis for investment decisions. Always consult with financial professionals before making investment choices.

---

**Happy Learning! 📚💡**
