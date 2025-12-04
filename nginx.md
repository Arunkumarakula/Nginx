# **Web Server**

* A web server is a software application that stores, processes, and delivers web pages to clients over the internet using protocols like HTTP/HTTPS.
* When a user sends a request through a browser, the web server receives the request, processes it, and sends back the appropriate response such as HTML pages, images, or data.

---

### **Webservers are used to:**

* Hosting Websites and Web Applications: It provides a platform to store website files and make them accessible online.
* Handling Client Requests: It processes HTTP requests and ensures that users receive the correct web resources.
* Performance & Scalability: Web servers manage multiple connections efficiently and support load balancing.
* Security: They offer features like SSL/HTTPS, firewalls, and access control to protect data.

---

* Web servers work on the request–response model**, where the client sends an HTTP request and the server processes it and returns an HTTP response.

---

# **HTTP**

*HTTP (HyperText Transfer Protocol)* is an application-layer protocol used for communication between clients and web servers on the internet.
It defines how requests and responses are formatted and transmitted, making it the foundation of data exchange on the World Wide Web.

* Stateless: Each request is independent the server does not store client session data by default.
* Request–Response Model: Clients send requests → Servers send responses.
* Flexible & Extensible: Supports various data formats like HTML, JSON, XML, images, videos, etc.

---

### **HTTP Status Codes**

* **1xx** – Informational
* **2xx** – Success (e.g., 200 OK)
* **3xx** – Redirection (e.g., 301 Moved Permanently)
* **4xx** – Client Errors (e.g., 404 Not Found)
* **5xx** – Server Errors (e.g., 500 Internal Server Error)

---

# **HTTPS**

*HTTPS (HyperText Transfer Protocol Secure)* is the secure version of HTTP.
It uses SSL/TLS encryption to ensure that the communication between a client and a web server is encrypted, authenticated, and protected from tampering.

* **encryption:** Data transferred is encrypted, so even if someone it cannot be read.
* **Authentication:** HTTPS verifies the identity of the website using an SSL/TLS certificate, preventing fake websites (phishing).
* **Data Integrity:** Ensures that data is not altered while in transit.
* **Secure Browser Indicators:** Browsers show a padlock icon and “https://” in the URL bar.

---

# **Webservers host and deliver static and dynamic content**

### **Static:**

Static content refers to fixed files such as HTML, CSS, images, or JavaScript that are delivered exactly as stored on the server without any server-side processing. Every user receives the same version of this content.

### **Dynamic:**

Dynamic content is generated on the server based on logic, user input, or database queries, meaning different users may receive different outputs. Dynamic content uses server-side technologies like PHP, Python, or Node.js.

**Examples:** User dashboards, E-commerce product listings, Social media feeds

---

# **Most Commonly Used Web Servers**

## **1. Apache HTTP Server:**

* Apache is one of the oldest, most popular, and stable open-source web servers.
* Highly modular supports add-on modules for security, caching, URL rewriting, etc.
* Extensive language support works well with PHP, Python, Perl, etc.
* Flexible configuration per-directory .htaccess control

---

## **2. Nginx:**

* Nginx is known for its performance, efficiency, and modern architecture.
* It was built specifically to solve the C10k problem (handling 10,000+ concurrent connections).

**High concurrency:**
Nginx uses an event-driven, asynchronous architecture, allowing it to handle many thousands of simultaneous connections with minimal resources.

**Low memory usage (lightweight):**
Because of its non-blocking design, Nginx requires very little RAM, making it ideal for high-traffic websites.

**Excellent for serving static content:**
Nginx delivers static files (HTML, images, CSS, JS) much faster than Apache, with less CPU and memory.

**Reverse proxy and load balancer:**
Nginx is commonly used as a reverse proxy in front of application servers.

**Flexible and extensible**

**Works perfectly in:**
Microservices, Containerized environments, High-performance cloud architectures

---

# **Nginx Default Ports**

*By default Nginx listens on port **80**, which uses the HTTP protocol.*
HTTP is not secure because it does not encrypt data meaning any sensitive information sent between the client and the server travels in plain text and can be intercepted.
To secure the communication, Nginx should be configured to use **HTTPS on port 443**, which encrypts data using SSL/TLS.

---

# **Nginx File Locations & Important Files**

* **/etc/nginx/** : This is the primary directory where almost all Nginx configuration files are stored.
* **/etc/nginx/nginx.conf** : This is the main configuration file that includes all other server and site configurations.
* **/usr/share/nginx/html/** : This is the default web root directory for Nginx. Any static files placed here (HTML, CSS, images) will be served by default.
* **/usr/share/nginx/html/index.html** : This is the default page that loads when you access the server’s IP or domain.

---

# **Reverse Proxy**

A reverse proxy is a server that sits between clients and backend servers. Instead of clients communicating directly with the application servers, all requests go through the reverse proxy first. It then forwards the request to the appropriate backend server and returns the response to the client.

Reverse proxies are commonly used for **security, load balancing, performance, and scalability**.

They help improve security by hiding server details and protecting against attacks like DDoS.
They provide scalability and flexibility through load balancing.
Reverse proxies can handle SSL/TLS encryption (SSL termination), reducing the burden on backend servers.
They can perform caching to speed up responses and reduce server load.

---

# **Load Balancing**

Nginx can act as a load balancer to distribute traffic across multiple backend servers, ensuring no single point of failure while providing scalability, fault tolerance, and high availability.

### **1. Round Robin (Default):**

* Requests are distributed evenly across all servers.
* Simple and effective when all servers have similar capacity.

**Example:**
1st request → Server A
2nd request → Server B
3rd request → Server C, then repeat.

**Use when:**

* All servers have equal performance and load capacity.


