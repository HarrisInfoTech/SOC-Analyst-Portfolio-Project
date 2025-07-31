 🧱 Week 1 – SOC Lab Setup & Fleet Integration

This week establishes the foundation of my SOC Analyst Lab as part of the 30-Day SOC Analyst Challenge. I designed the lab architecture, installed Elastic Stack (ELK), deployed a Windows Server endpoint, and connected it to Fleet using Elastic Agent.

---

## 📅 Day 1 – Lab Planning & Architecture

🎯 **Goal:** Design a virtual SOC lab to simulate endpoint monitoring and log aggregation.

### 🖥️ Lab Components

| Host                | Purpose                        | Tool/OS                   |
|---------------------|--------------------------------|---------------------------|
| Windows Server      | Endpoint log source            | Windows Server 2022       |
| Ubuntu Server       | SIEM & dashboard               | Elasticsearch, Kibana     |
| Fleet Server        | Agent coordination & policies  | Elastic Fleet             |
| Analyst Workstation | SOC investigation hub          | Web browser, Kibana       |

📌 Lab diagram created using [draw.io](https://draw.io).

📸 *Screenshot: `lab-diagram.png`*

---

## 📅 Day 2 – ELK Stack Setup

🎯 **Goal:** Set up Elasticsearch and Kibana on Ubuntu Server.

### 🔧 Install Steps

```bash
sudo apt update && sudo apt upgrade -y
sudo apt install elasticsearch kibana -y
sudo systemctl enable elasticsearch --now
sudo systemctl enable kibana --now

