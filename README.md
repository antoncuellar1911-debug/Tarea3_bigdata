# Tarea 3 - Procesamiento de Datos con Apache Spark y Kafka

Este repositorio contiene la solución práctica para la Tarea 3 del curso de Big Data.

## Estructura del Código

- `procesamiento_batch.py`: Script para la carga, limpieza y análisis exploratorio (EDA) de datos masivos en batch utilizando PySpark.
- `kafka_producer.py`: Productor en Python que simula y envía eventos de sensores en tiempo real hacia un topic de Apache Kafka.
- `spark_streaming_consumer.py`: Consumidor en Spark Streaming que lee los eventos de Kafka y calcula estadísticas de promedio por ventanas de tiempo.

## Requisitos y Ejecución
- Apache Spark 3.5.3
- Apache Kafka 3.6.2
- Python 3 / `kafka-python`

### Ejecución Streaming:
1. Iniciar ZooKeeper y broker de Kafka.
2. Iniciar el productor: `python3 kafka_producer.py`
3. Iniciar el consumidor Spark: `spark-submit --packages org.apache.spark:spark-sql-kafka-0-10_2.12:3.5.3 spark_streaming_consumer.py`
