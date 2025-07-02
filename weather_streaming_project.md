## 🌦️ Real-Time Weather Streaming with Apache Kafka & Flink

### 🧠 **Project Objective**

This project demonstrates how to build a **real-time data streaming pipeline** using **Apache Kafka** and **Apache Flink**, with live or near-real-time weather data as the input stream. The goal is to simulate a production-grade streaming system, showcasing event ingestion, processing, and output to a storage or visualization layer.

---

### 📡 **Data Source**

- **UK Met Office DataPoint API** and/or **OpenWeatherMap API**
- Periodically polled weather observations (temperature, wind, rain, etc.) for UK locations
- Data is treated as a simulated real-time stream and pushed into Kafka topics

---

### 🛠️ **Technology Stack**

| Component         | Technology                     | Purpose                                   |
| ----------------- | ------------------------------ | ----------------------------------------- |
| Event Streaming   | **Apache Kafka**               | Ingest and distribute weather events      |
| Stream Processing | **Apache Flink**               | Stateful processing, windowing, analytics |
| Producer Script   | **Python** + Kafka client      | Pulls data from API and produces to Kafka |
| Sink (optional)   | PostgreSQL / Files / Dashboard | Output of processed data for inspection   |
| Orchestration     | **Docker Compose**             | Local environment setup                   |
| Monitoring (opt)  | Grafana / CLI / Logs           | Visualize output, system performance      |

---

### 📈 **Learning Outcomes**

By completing this project, I aim to:

- Understand how to design and implement **event-driven pipelines**
- Gain hands-on experience with **Apache Kafka** (brokers, topics, producers, consumers)
- Develop and deploy **Flink jobs** for real-time processing
- Practice working with **event time**, **windowing**, and **stateful stream processing**
- Explore strategies for **joining** streams and **detecting anomalies**
- Learn how to manage streaming pipelines using **Docker** and modern DevOps tools
- Prepare a portfolio-ready project that reflects **real-world data engineering skills**

---

### ⚙️ **System Setup**

```
[Weather API Poller (Python)]
            |
            v
     [Kafka Topic: "uk-weather"]
            |
            v
     [Flink Job: process-weather]
            |
            v
[Sink: Console, PostgreSQL, or Dashboard]
```

- The **Python Kafka producer** polls the weather API every X minutes
- Weather data is published into a Kafka topic
- A **Flink job** processes the stream, e.g., filtering, aggregating, or enriching
- Processed results are written to an output sink (e.g., database, file, or dashboard)

