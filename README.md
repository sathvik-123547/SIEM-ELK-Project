
# SIEM-ELK Project

## 📌 Overview
This project demonstrates how to build a **Security Information and Event Management (SIEM)** system using the **ELK Stack** (Elasticsearch, Logstash, Kibana) along with **Filebeat** for log forwarding and **ElastAlert2** for alerting. It simulates authentication logs, ingests them through the pipeline, indexes them in Elasticsearch, visualizes them in Kibana, and generates alerts when suspicious activity is detected.

---

## 🛠️ Tech Stack
- **Python** → Custom log generator (simulates SSH login attempts)  
- **Filebeat** → Lightweight log shipper that forwards logs to Logstash  
- **Logstash** → Parses logs using **grok filters**, enriches fields, and forwards data to Elasticsearch  
- **Elasticsearch** → Stores, indexes, and allows searching of log data  
- **Kibana** → Visualization dashboard to explore and analyze logs  
- **ElastAlert2** → Rule-based alerting engine integrated with Elasticsearch  
- **Docker & Docker-Compose** → Containerized deployment for all services  

---

## 🚀 Setup Instructions
### 1. Clone the Repository

git clone https://github.com/sathvik-123547/SIEM-ELK-Project.git
cd SIEM-ELK-Project


### 2. Start the Stack

docker-compose up -d


### 3. Verify Containers

docker ps

You should see running containers for **Elasticsearch, Kibana, Logstash, Filebeat, and ElastAlert2**.

### 4. Generate Logs

Run the Python log generator to simulate SSH login attempts:

python log_generator.py

### 5. Access Kibana

Open [http://localhost:5601](http://localhost:5601)

* Create an **Index Pattern** for `filebeat-*` and `elastalert_status`.
* Explore logs in **Discover**.
* Build **dashboards** for failed/successful SSH login attempts.

### 6. Alerts

ElastAlert2 periodically queries Elasticsearch for suspicious patterns (e.g., multiple failed logins).
Alerts are stored in the `elastalert_status` index, viewable in Kibana.

---

## 📊 Features

* ✅ End-to-end log ingestion pipeline with ELK
* ✅ Realistic log simulation via Python
* ✅ Custom **Logstash Grok filters** for parsing
* ✅ Visual dashboards in Kibana
* ✅ Automated alerting with ElastAlert2
* ✅ Fully containerized with Docker

---

## 📌 Learning Outcomes

* Hands-on experience with SIEM architecture
* Understanding log ingestion and parsing
* Building Kibana dashboards for monitoring
* Creating alerting rules for security use cases
* Using Docker to orchestrate multi-service security projects

---

## 🔮 Future Improvements

* Add real-world log sources (e.g., system, web, firewall logs)
* Integrate email/Slack alerts in ElastAlert
* Expand rule sets for detecting brute-force attacks and anomalies
* Deploy on cloud (AWS/Azure) for scalability

---

## 👨‍💻 Author

**Sathvik**
🔗 [GitHub Profile](https://github.com/sathvik-123547)

```

