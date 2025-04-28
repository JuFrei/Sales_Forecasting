# Sales Forecasting with XGBoost and Stacking

This project explores different modeling strategies for forecasting sales, using XGBoost regressors and a stacking ensemble approach.  

## Project Structure
- **Model 1**: One global model trained on all historical data.
- **Model 2**: One global model trained only on recent data.
- **Model 3**: Separate model for each product family, trained on all historical data.
- **Model 4**: Separate model for each product family, trained only on recent data.

## Key Results
| Model   | RMSLE   | Notes                                              |
|---------|---------|----------------------------------------------------|
| Model 1 | 0.6333  | Single global model on full historical dataset     |
| Model 2 | 0.5277  | Single global model on recent data split           |
| Model 3 | 0.4128  | Separate model per family on full historical data  |
| Model 4 | 0.4152  | Separate model per family on recent data split     |

## Approach
- Feature engineering included promotions, holidays, and oil price data.
- Models were trained using XGBoost regressors.
- Stacking was applied by using family-level model outputs as meta-features for a second-stage model.
- Evaluation metric: Root Mean Squared Log Error (RMSLE).
