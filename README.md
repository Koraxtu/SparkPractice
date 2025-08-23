1. docker compose up -d
# spark-shell against the master:
2. docker run --rm -it --network host bitnami/spark:latest \
3. spark-shell --master spark://localhost:7077
# Tear down when done
4. docker compose down -v