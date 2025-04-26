# Hunting Hypothesis – Brute Force Login Attempts

## 🎯 Hypothesis
Adversaries may be attempting brute force attacks against public web-facing login portals.

## 🔎 Hunting Method
- Filter for multiple HTTP 401 status codes from the same IP
- Identify accounts accessed successfully after multiple failures
- Highlight suspicious user agents (curl, python, sqlmap)

## 🔧 Data Sources
- Apache web server logs
- Splunk (via saved searches or dashboards)
- GeoIP (optional)

## 🧠 Why This Matters
Brute force login attempts are often early-stage attacks and can lead to credential compromise or lateral movement.
