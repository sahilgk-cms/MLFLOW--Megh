# MLFLOW--EC2

## Project overview
- Integrate ml model training with MLFLLOW in AWS EC2 + dockerized container.
- The EC2 instance used is PH-Vector-Database.

## Project description
- Theere are 5 config yml files which can be changed.
- they are
    - config/data/data_v1.yml
    - config/database/db_v1.yml
    - config/features/features_v1.yml
    - config/ml/ml_v1.yml
    - config/search_spaces/search_spaces_v1.yml
- Rest of env.py, filepaths.py remain constant.
- I have already set up the mlflow server on port 5000
  
## How to run
- Login to the EC2 instance using ssh.
- I have already kept the mlflow-server running.
- Run the pipeline thorugh docker compose
```
docker-compose up ml-pipeline
```



## Future improvements
- Migrate artifact store to S3 (as artifacts cannot be accessed outside of EC2 instance)
- Replace SQLite with PostgreSQL 
