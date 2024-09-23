# Chapter Five: Understanding Web Requests | *uebu rikuesuto ウェブリクエスト* 

![Web Requests](https://github.com/user-attachments/assets/187bf552-8f33-4949-b4e5-47b36235a2df)

### *This post is currently under construction.*

# Web Request Basics

Whether you are aware of it or not, thousands of web requests are likely taking place in your hand each and every day, if you use apps on your phone. Both mobile and web apps are constantly interacting with the internet. That communication happens primarily through web requests and the HTTP protocol.

Communication via HTTP involves two parties, a client and a server. The client (the device you’re using) sends a request for information or action to a server (a computer that stores and provides resources). The server processes the request and returns the requested resource to the client. 

This process is fundamental to how the internet works, enabling the retrieval and display of web pages, the submission of form data, and much more.

## Visiting a Website

Let’s say you’re getting ready to apply to colleges. One of the first things you might want to do before you decide to apply to a school is visit that schools website. Hypothetically, you are looking for a school with a small enrollment, high acceptance rate, and adventure so you decide that you want to learn more about [Alaska Pacific University](https://www.alaskapacific.edu/). You open up your preferred web browser and type in the URL alaskapacific.edu.

What happens next are a number of steps that take place at dizzying speeds to display the website in your browser almost instantaneously (in many cases inside the U.S. and other developed nations).  If this is the first time you are visiting the site, your computer (the client) sends a request to a DNS ([Domain Name System](https://www.cloudflare.com/learning/dns/what-is-dns/)) server to translate the URL into an [IP address](https://en.wikipedia.org/wiki/IP_address). The client sends the URL and the DNS server returns the IP address. 

Once your web browser has the IP address, it sends a GET request to a web server via port 80, the default port for HTTP, asking for the root path (/). The root path is the location where all of the website’s files and information are saved. The web server processes the request, reads and returns the contents of the [index file](https://www.thoughtco.com/index-html-page-3466505) to your browser in an HTTP response. The browser then renders the index file to the website that appears on your screen. 

This all takes place in a matter of seconds and it is not just visiting websites that utilizes these requests. Whether you're browsing a website, sending an email, or streaming a video, web requests are constantly at work behind the scenes. 

## The Request-Response Cycle

As you can see from the example above, when a web request is made, a cycle is initiated:

1. The client sends a request to the server
2. The server processes the request
3. The server sends back a response
4. The client receives and processes the response

## Anatomy of a Web Request

A typical web request consists of several key components:

- **URL:** The address of the resource being requested
- **Headers:** Additional information about the request or the client
- **Method:** The type of request (GET, POST, etc.)
- **Body:** Optional data sent with the request (common in POST requests)

## Types of Web Requests

There are several types of web requests, each serving a different purpose:

- **GET:** Used to retrieve information from a server
- **POST:** Used to submit data to be processed by the server
- **PUT:** Used to update existing resources on the server
- **DELETE:** Used to remove a resource from the server
- **HEAD:** Similar to GET but retrieves only headers, not the body of the response

## Importance for Blue Teamers

Understanding web requests is a fundamental skill for security professionals because web-based attacks are a primary vector for malicious activity. Knowledge of web requests enable blue teamers to:

### - Recognize Malicious Activity
  - Web-based attacks like cross-site scripting, SQL injection, and cross-site request forgery try to exploit vulnerabilities in how web applications handle requests. Understanding the structure of HTTP requests and responses helps defenders spot abnormal activity indicative of these tyoes of attacks.
 
### - Identify Vulnerabilities
  - Knowing how web requests interact with a server and its applications allows security professionals to identify potential weaknesses in the way data is handled, including analyzing GET/POST requests.
    
  - Understanding how data flows between client and server enables defenders to spot issues like unencrypted transmissions.

### - Mitigate & Respond to Attacks
  - During an incident, clear analysis of web traffic logs will help to understand the attacker's actions and vectors. It can assist in tracing the attack, identifying compromised areas, or determioning how the attack was delivered.
    
  -   Analyzing request patterns, header manipulation, and other abnormalities can help to identify whether the attack is part of a broader strategy.

### - Understand Attack Methods
  - Many attacks leverage web requests to deliver payloads, execute malicious scripts, or manipulate a system. Knowledge of how web requests are crafted helps blue teamers understand how phishing, malware injection, and botnets operate in real-world scenarios

### - Harden Web Applications
  - To secure web applications effectively, defenders need to know how developers may inadvertently expose the system to attacks. This includes insecure use of cookies, improper request validation, or insecure session handling.
    
  - Knowledge of how web requests are built and processed enables cybersecurity professionals to suggest coding best practices, such as validating inputs, using HTTPS, and implementing secure session management.

### - Support Incident Response & Forensics
  - When a breach or attack occurs, log analysis and packet captures are key tools for cybersecurity teams. Knowing how web requests look at different stages of an attack helps analysts reconstruct what happened and supports faster remediation.

  - Web requests provide crucial evidence for forensic analysis, enabling professionals to attribute attacks and understand attackers' tactics, techniques, and procedures (TTPs).

In summary, understanding web requests empowers defensive cybersecurity professionals to identify, block, and respond to web-based threats, while also helping them to secure applications and networks more effectively.
