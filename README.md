Sign Burger – Performance Testing with Apache JMeter (100k User Load)

This repository contains the complete setup, configuration, and reporting artifacts for conducting a large-scale performance test (100,000 users) on the **Sign Burger** application using **Apache JMeter**.

### 🔍 Overview

* **Objective:** Evaluate backend performance of the Login API under high user load (100k users).
* **Tool Used:** Apache JMeter 5.6.3
* **Deployment:** CLI mode (preferred for high concurrency) with HTML reporting
* **Report Hosting:** [Netlify](https://delightful-fox-4d5929.netlify.app)

---

### 📁 Folder Structure

```
├── jmeter/
│   ├── otp-login-test.jmx          # JMeter Test Plan (Bypassed OTP)
│   ├── results/
│   │   ├── result_100k.jtl         # Raw test results
│   │   ├── html_100k/              # HTML report folder
├── docs/
│   ├── Sign_Burger_Performance_Test_Summary.pdf  # Final test summary report
```

---

### 🚀 How to Run the Test (CLI Mode)

```bash
cd /path/to/jmeter/bin
./jmeter -n -t "otp-login-test.jmx" -l "results/result_100k.jtl" -e -o "results/html_100k"
```

> Note: Ensure the `results/` and `html_100k/` folders are pre-created or writable.

---

### 📊 Performance Summary

* **Total Requests:** 100,000
* **Success Rate:** 99.998%
* **Avg Response Time:** 2.2 sec
* **P90:** 10.2 sec | **P95:** 13.2 sec | **P99:** 7.2 sec
* **Max Response Time:** 30 sec
* **Throughput:** \~49.6 RPS

---

 Key Notes

* OTP API was **bypassed** for performance accuracy.
* Testing conducted on **Docker-hosted JMeter** for stability beyond 8,000 concurrent users.
* CLI preferred for stable execution at high loads.
* Hosted full report on Netlify for easy access.

 Report Link

🔗 [View Full HTML Report](https://delightful-fox-4d5929.netlify.app)

