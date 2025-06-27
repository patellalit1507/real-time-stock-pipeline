# Real-Time Stock Market Data Pipeline

## Overview
This project builds a real-time stock market data pipeline to ingest, process, store, and visualize stock market data. It uses Polygon.io for data ingestion, Apache Kafka for streaming, Apache Spark for processing, Snowflake for storage, Apache Airflow for orchestration, and Tableau for visualization. The pipeline is deployed on AWS for scalability.

## Tech Stack
- **Ingestion**: Python, Polygon.io WebSocket API
- **Streaming**: Apache Kafka
- **Processing**: Apache Spark (PySpark)
- **Storage**: Snowflake
- **Orchestration**: Apache Airflow
- **Visualization**: Tableau
- **Cloud**: AWS (EC2/EKS)
- **Version Control**: GitHub

## Setup Instructions
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/real-time-stock-pipeline.git
   cd real-time-stock-pipeline
   ```
2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
3. **Configure Environment**:
   - Set up `.env` with API keys and credentials (see `.env.example`).
4. **Run the Pipeline**:
   - Start Kafka, Spark, and Airflow services (see `deploy/` for scripts).
   - Run the ingestion script: `python src/ingestion/ingest_data.py`.

## Folder Structure
```
real-time-stock-pipeline/
├── src/
│   ├── ingestion/           # Data ingestion scripts (Polygon.io WebSocket)
│   ├── processing/          # Spark processing scripts
│   ├── storage/             # Snowflake connection and storage scripts
│   ├── orchestration/       # Airflow DAGs
│   ├── visualization/       # Tableau or Plotly Dash scripts
├── deploy/                  # AWS deployment scripts (Docker, Kubernetes)
├── config/                  # Configuration files (Kafka, Spark, Snowflake)
├── tests/                   # Unit and integration tests
├── docs/                    # Documentation and architecture diagrams
├── .env.example             # Example environment variables
├── requirements.txt         # Python dependencies
├── README.md                # Project documentation
├── LICENSE                  # License file
└── .gitignore               # Git ignore file
```

## Next Steps
- Configure AWS credentials and Snowflake account.
- Deploy Kafka and Spark clusters on AWS EKS.
- Connect Tableau to Snowflake for visualization.