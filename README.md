# 🎯 Splunk DNS Log Analysis Lab

Welcome to the **Splunk DNS Log Analysis Lab**! This hands-on lab teaches you how to ingest, parse, and analyze DNS logs in Splunk to uncover patterns, anomalies, and security-relevant insights.  

---

## 📝 **Objective**
By completing this lab, you will:  
- 🛠️ Learn to ingest Zeek-style JSON DNS logs into Splunk  
- 🔍 Extract valuable information: query types, source hosts, and frequently queried domains  
- 🧩 Build SPL (Search Processing Language) queries for investigative analysis  
- 🚨 Detect anomalies: failed resolutions, suspicious queries, and high-latency lookups  
- 📊 Visualize DNS activity through dashboards and reports  

---

## 🖥️ **Lab Setup**
Before starting, ensure you have the following:  
- ✅ **Splunk installed and accessible**  
- ✅ **JSON-formatted Zeek DNS logs** (`dns_logs.json`)  

**Setup Steps:**  
1. Download `dns_logs.json` and place it in the `lab/` directory  
2. Go to Splunk Web → **Settings > Add Data**  
3. Upload the file and set **Source type**: `json` (or create a custom sourcetype like `zeek:dns`)  
4. Choose **Index**: `main` or create a new index `dns_lab`  
5. Verify indexing with:
```spl
index=dns_lab | head 5
