# Comex Automation Portfolio

Automation projects built with n8n focused on Foreign Trade operations.

---

## Project 1 — FX Rate Monitor (USD/BRL)

### Problem
Manually checking exchange rates is time-consuming and easy to miss critical thresholds that impact import costs.

### Solution
Automated workflow that checks the USD/BRL exchange rate every hour and sends an email alert when it exceeds a defined limit.

### Tools
- n8n (local)
- AwesomeAPI (free FX rate API)
- Gmail

### Workflow
Schedule Trigger → HTTP Request → IF → Gmail
<img width="1728" height="734" alt="image" src="https://github.com/user-attachments/assets/209f5bbe-3eca-4551-9b02-7dd56b7c4c4e" />

### How it works
1. Schedule Trigger fires every hour
2. HTTP Request fetches live USD/BRL rate from AwesomeAPI
3. IF node checks if rate exceeds threshold (e.g. R$ 5.10)
4. Gmail sends an alert email with current rate, daily high and low

---

*Built by Leonardo Nobrega — Foreign Trade MBA | International Relations 
