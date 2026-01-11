
# ML System Design Outline (Interview)

## 1) Goal
- What are we predicting / generating?
- What metric defines success?
- What constraints exist (latency, cost, privacy)?

## 2) Data
- Where does training data come from?
- How is it labeled?
- How do we prevent leakage?
- How do we detect drift?

## 3) Training Pipeline
- Preprocessing steps
- Feature engineering
- Model choice + baseline
- Experiment tracking
- Model registry (optional)

## 4) Serving
- Online vs batch
- API endpoints
- Scaling strategy
- Caching (if relevant)

## 5) Monitoring
- Data quality checks
- Prediction drift
- Performance metrics (delayed labels)
- Alert thresholds

## 6) Retraining
- Trigger strategy (schedule + drift + performance)
- Rollback plan
