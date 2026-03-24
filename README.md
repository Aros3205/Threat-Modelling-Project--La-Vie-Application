# Threat-Modelling-Project-La Vié-Application



## 📌 Overview
This project demonstrates a complete threat modelling exercise performed on a web-based application (**La Vié App**) using two industry-recognized tools:

- Microsoft Threat Modeling Tool (MTMT)
- OWASP Threat Dragon

The goal was to identify potential security threats, categorize them using the STRIDE model, and propose effective mitigations.

---

## 🏗️ System Architecture (DFD)


### All Users (External Entity)


In this project:

The **All Users** entity represents any individual interacting with the application from outside the system boundary. This includes both authorized and unauthorized users attempting to access the application.

All Users initiate HTTP requests to the system and receive responses from the backend. This entity is critical in threat modeling because it represents the primary entry point for potential attacks such as spoofing, injection, and unauthorized access.


- Authorized users send legitimate requests and receive valid responses.
- Unauthorized users may attempt malicious actions such as SQL injection, spoofing, or excessive requests.

This entity lies outside the trust boundary, making all incoming data from this source untrusted and requiring validation and security controls.


The application consists of:

- External Users (Authorized & Unauthorized)
- Backend Web Server
- SQL Database
- Trust Boundary separating frontend and backend systems

### 🔹 Key Data Flows:
- HTTP Requests/Responses between users and backend
- API communication between frontend and backend
- SQL queries between backend server and database

---

## 🧰 Tools Used

| Tool | Purpose |
|------|--------|
| OWASP Threat Dragon | Manual threat modeling and visualization |
| Microsoft Threat Modeling Tool (MTMT) | Automated threat generation and analysis |

---

## ⚠️ Threat Modeling Approach

The STRIDE model was used to classify threats:

- **S** – Spoofing  
- **T** – Tampering  
- **R** – Repudiation  
- **I** – Information Disclosure  
- **D** – Denial of Service  
- **E** – Elevation of Privilege  

---

## 🔍 Identified Threats

### 1. Spoofing
Attackers may impersonate legitimate users to gain unauthorized access.

**Mitigation:**
- Implement strong authentication (e.g., MFA)
- Use secure session management
- Enforce identity verification mechanisms

---

### 2. Tampering
Data may be altered during transmission or through malicious input (e.g., SQL injection).

**Mitigation:**
- Use input validation and sanitization
- Implement parameterized queries
- Use HTTPS to protect data in transit

---

### 3. Repudiation
Users may deny performing certain actions due to lack of proper logging.

**Mitigation:**
- Enable logging and monitoring
- Maintain audit trails
- Use timestamps and user activity tracking

---

### 4. Information Disclosure
Sensitive data may be exposed to unauthorized users.

**Mitigation:**
- Encrypt data in transit (HTTPS)
- Use proper access controls
- Avoid exposing sensitive data in responses

---

### 5. Denial of Service (DoS)
Attackers may overwhelm the system with excessive requests.

**Mitigation:**
- Implement rate limiting
- Use load balancing
- Monitor traffic and apply throttling

---

### 6. Elevation of Privilege
Attackers may gain higher-level permissions than intended.

**Mitigation:**
- Enforce role-based access control (RBAC)
- Apply the principle of least privilege
- Regularly audit permissions and system access
---

## 📊 Outputs




### 🔹 OWASP Threat Dragon


#### System Diagram


![OWASP Diagram](screenshots/owasp-diagram.png)



#### SQL Injection Threat


![OWASP SQL Injection](screenshots/owasp-sql-injection.png)



#### Spoofing Threat


![OWASP Spoofing](screenshots/owasp-spoofing.png)

---

### 🔹 Microsoft Threat Modeling Tool (MTMT)



#### System Diagram


![MTMT Diagram](screenshots/mtmt-diagram.png)



#### Threat Summary


![MTMT Threat Summary](screenshots/mtmt-threat-summary.png)



#### SQL Injection Threat


![MTMT SQL Injection](screenshots/mtmt-sql-injection.png) 



## 📄 Reports

- ![OWASP Threat Model Report](reports/owasp-report.pdf)
- ![MTMT Threat Model Report](reports/mtmt-report.pdf)

---

## 🎯 Key Learnings

- Understanding how data flows across trust boundaries  
- Identifying vulnerabilities using STRIDE methodology  
- Differentiating between automated vs manual threat modeling  
- Applying practical mitigations to real-world scenarios  

---

## 🚀 Conclusion

This project demonstrates practical experience in:

- Threat modeling  
- Secure system design  
- Risk identification and mitigation  

This threat modeling exercise applies the STRIDE methodology to systematically identify and analyze potential security risks within the La Vie Application. By examining data flows, trust boundaries, and system interactions, key threats across all STRIDE categories were identified, including spoofing, tampering, repudiation, information disclosure, denial of service, and elevation of privilege.

Each identified threat is paired with practical mitigation strategies to reduce risk and improve the overall security posture of the system. This approach ensures a structured and comprehensive evaluation of potential vulnerabilities, aligning with industry best practices for secure system design.

---

## 👤 Author

**[Tolulope R Arowobusoye]**  
Cybersecurity Enthusiast | Threat Modeling | Application Security  

---
