# Hunt Summary – Brute Force Activity

## 🔍 Key Findings

- IP `203.0.113.99` generated 4 failed login attempts in 10 seconds using `curl/7.58.0`
- One successful login followed the failures
- Endpoint `/wp-login.php` accessed by IP `198.51.100.77` using user-agent `sqlmap`

## 🔐 Analyst Recommendations

- Block `203.0.113.99` at network edge
- Force password reset for affected accounts
- Add alerting for multiple 401s from a single IP in short timeframes
- Educate users on MFA and strong password practices

## 📅 Follow-up

- Conduct similar hunt on other externally-facing logs (e.g., VPN, RDP)
- Tune Sigma rules to reduce false positives
