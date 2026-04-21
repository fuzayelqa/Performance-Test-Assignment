# 🧪 Apache JMeter Performance Testing Report  
       
📘 **Project Overview**
This project demonstrates performance testing of the **OrangeHRM Demo Application** using **Apache JMeter**.  
 
The purpose of this test was to analyze: 
 
- 🚀 Application performance under load 
- ⚡ Error rate and response time behavior   
- 🛡️ Stability of the server under stress

--- 
  
## ⚙️ Test Environment

| Parameter           | Description                               |
|--------------------|-------------------------------------------|
| **Tool**            | Apache JMeter (Non-GUI Mode)              |
| **Target Application** | OrangeHRM Demo                          |
| **Test Duration**   | 35 minutes                                |
| **Total Requests**  | 30,000                                     |
| **Threads (Users)** | Variable                                  |
| **Report Generated**| PDF Summary & Dashboard                   |

---

## 🧾 Test Summary

| Metric              | Result                                |
|-------------------|----------------------------------------|
| **Total Requests**     | 30,000                                 |
| **Passed Requests**    | 29,966 (99.89%)                        |
| **Failed Requests**    | 34 (0.11%)                              |
| **Error Rate**         | 0.11%                                   |
| **APDEX Score**        | 0.696 (Average Performance)            |

---

## 📊 Error Breakdown

| Error Type                  | Count | Percentage | Description                          |
|-----------------------------|-------|------------|--------------------------------------|
| 500 Internal Server Error    | 32    | 100%       | Internal server error on endpoints   |

---

## 🧠 Analysis

- ✅ The system performed well with **99.89% of requests passing**.  
- ⚠️ Most failures were due to **500/Internal Server Errors**, indicating occasional backend instability.  
- 📈 APDEX score of **0.696** indicates average user experience.  
- ⏱ Response times for key endpoints ranged from **375ms to 1.4s**.  

---

## 🛠️ Recommendations

- Investigate backend causes of 500 errors.  
- Optimize server resources and database queries to reduce latency.  
- Implement monitoring for endpoints with higher failures or response time spikes.  
- Perform periodic load tests to ensure consistent performance.  

---

## 📁 Files Included

| File                            | Description                                |
|--------------------------------|--------------------------------------------|
| `testplan.jmx`                  | JMeter Test Plan                            |
| `results.jtl`                   | Test Result Log File                         |
| `Apache_JMeter_Test_Report.pdf` | Performance Test Summary Report (PDF)       |
| `README.md`                     | Documentation File                          |

---

## 🚀 How to Run the Test (CLI Mode)

Run the JMeter test in Non-GUI Mode using:

```bash
jmeter -n -t testplan.jmx -l results.jtl -e -o Reports/

