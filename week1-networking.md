
  # 🌐 Week 1: Networking & Web Basics (Deep Dive with Examples)

Welcome to Week 1 of your System Design Roadmap!  
In this module, we’ll focus on the foundational networking concepts that drive the web and all modern systems.

---

## 📘 Topics to Learn

---

### 1️⃣ Client-Server Model

**Concept**:  
A *client* sends a request, and the *server* responds.

**Real-World Analogy**:  
You (client) call Domino’s (server) and order pizza. Domino’s processes your request and delivers it.

**Example**:
- Client: Browser / Mobile App / Postman
- Server: ASP.NET Core Web API
- Request: `GET /weatherforecast`
- Response: JSON weather data

---

### 2️⃣ IP Address

**Concept**:  
A unique address for every device on the internet.

**Example**:
- IPv4: `192.168.1.10`
- IPv6: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`

```bash
# To find your IP:
ipconfig        # Windows
ifconfig        # Linux/macOS
3️⃣ DNS (Domain Name System)
Concept:
Translates domain names (like google.com) into IP addresses.

Example:

bash
Always show details

Copy
nslookup google.com
Output:

yaml
Always show details

Copy
Server:  dns.google
Address:  8.8.8.8

Non-authoritative answer:
Name:    google.com
Address:  142.250.67.142
4️⃣ HTTP vs HTTPS
Feature	HTTP	HTTPS
Secure?	❌ No	✅ Yes (uses TLS/SSL)
Port	80	443
Visible in transit?	Yes	No (Encrypted)
Example:

HTTP: http://yourapi.com

HTTPS: https://yourapi.com

5️⃣ Latency
Concept:
Time taken from sending a request to receiving a response.

Measured in: milliseconds (ms)

bash
Always show details

Copy
ping google.com
Output:

sql
Always show details

Copy
Reply from 142.250.67.142: time=24ms
6️⃣ Proxy vs Reverse Proxy
Type	Proxy	Reverse Proxy
Purpose	Hides client from server	Hides server from client
Example	Corporate proxy filters traffic	Nginx reverse proxy load balancer
Tools	Squid	Nginx, HAProxy, API Gateway
Diagram:

text
Always show details

Copy
Client --> Proxy --> Server

Client --> Reverse Proxy --> Multiple Servers
🔧 Tools to Explore
Tool	Use Case
Postman	Test and debug HTTP APIs
Fiddler	Monitor and modify HTTP traffic
curl	Command-line API testing
ping	Test basic network latency
nslookup	Check DNS resolution
tracert	Show request hops to a server
🛠️ Hands-On Practice
🔹 1. Create a Simple ASP.NET Core Web API
bash
Always show details

Copy
dotnet new webapi -n NetBasicsDemo
cd NetBasicsDemo
dotnet run
Access it at:
https://localhost:5001/weatherforecast

🔹 2. Test API Using Postman
Open Postman.

Make a GET request to:
https://localhost:5001/weatherforecast

Check:

Headers

Latency

Status Code

Response Body

🔹 3. View Headers in Chrome DevTools
Open the browser.

Press F12 → Go to Network tab.

Refresh the page.

Click any request and view:

Request Headers

Response Headers

Timing / Latency

🔹 4. Try DNS & Latency Commands
bash
Always show details

Copy
nslookup openai.com
ping openai.com
tracert openai.com    # (Windows)
traceroute openai.com # (macOS/Linux)
