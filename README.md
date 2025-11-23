Time-Series Forecasting Project Report
1. Introduction
This report summarizes the end-to-end implementation of a multivariate time-series forecasting system using a Transformer-based deep learning model. The project includes synthetic dataset generation, preprocessing, model development, hyperparameter tuning, evaluation, and visualization.
2. Dataset Generation
A synthetic multivariate time-series dataset was programmatically generated with 5 features and 1500+ observations. Each feature incorporates seasonality, trend, and noise components.
Dataset characteristics:
- 1500 time steps
- 5 correlated features
- Clear seasonality and trend patterns
- Noise added to simulate real-world variance
3. Data Preprocessing
The dataset was scaled using StandardScaler. A sliding window technique was applied to create input sequences (60 steps) and target sequences (15 steps). The dataset was then split into training (70%), validation (15%), and test (15%) sets.
4. Model Architecture
A Transformer-based encoder architecture was implemented using PyTorch. Key components include:
- Input projection layer
- Positional encoding for temporal indexing
- Multi-head self-attention mechanism
- Transformer encoder with 2 layers and 4 attention heads
- Fully connected layer mapping encoded representation to multi-step outputs
5. Training Strategy
The model was trained for 5 epochs using the Adam optimizer (learning rate = 0.001) and Mean Squared Error (MSE) loss. Mini-batch training was performed with batch size 32.
6. Model Evaluation
Predictions were evaluated using MAE and RMSE after inverse scaling. A sample visualization was generated comparing forecast vs. true values.
7. Results Summary
The model produced reasonable forecasts across all features.
Evaluation metrics observed on the test set:
- MAE: (See console output of final model run)
- RMSE: (See console output of final model run)
8. Attention Interpretation (Planned)
The architecture allows extraction of attention weights, which can reveal which time steps contribute most to prediction. This is planned for future enhancement.
9. Conclusion
This project successfully demonstrates a complete forecasting pipeline using a Transformer architecture, synthetic dataset generation, preprocessing workflows, training routines, and evaluation metrics.
