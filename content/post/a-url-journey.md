---
date: 2024-09-02T13:17:27-04:00
title: 'A URL Journey'
draft: true
description: 'What happens when you type a URL into a browser?'
featured_image: '/images/AdobeStock_822553479_Preview.jpeg'
tags: [web, networking]
---

I was recently asked, "What happens when you type a URL into your browser?" It's a question that always makes me pause, trying to gauge the right level of detail. This time, I clearly missed the mark. In hindsight, I should have asked some clarifying questions to better understand the depth of knowledge the person was seeking. It's a lesson I know well, but sometimes, in the heat of the moment, even the simplest things can trip us up.

Inspired by this experience, I decided to dive deep into the answer myself. This article is the culmination of that research. So, the next time someone asks you the same question, you'll be ready to give a thorough response – after asking the appropriate clarifying questions, of course!

 ## DNS Resolution
The client starts by resolving the domain name of the website to an IP address using DNS (Domain Name System).

## TCP Handshake 
The client initiates a TCP connection with the server using a three-way handshake:

    - **SYN**: The client sends a SYN (synchronize) packet to the server to request a connection.

    - **SYN-ACK**: The server responds with a SYN-ACK (synchronize-acknowledge) packet to acknowledge the request.

    - **ACK**: The client sends an ACK (acknowledge) packet to establish the connection.

## HTTP Request
Once the TCP connection is established, the client sends an HTTP GET request to the server to request the web page.

## Server Processing
The server processes the request, retrieves the requested web page, and prepares an HTTP response. (This is usually the only latency most SWE's think about and control!)

## HTTP Response
The server sends the HTTP response back to the client, which includes the requested web page content.

## TCP Teardown
After the data transfer is complete, the client and server close the TCP connection using a four-way handshake:

    - **FIN**: The client sends a FIN (finish) packet to the server to terminate the connection.

    - **ACK**: The server acknowledges the FIN packet with an ACK.

    - **FIN**: The server sends a FIN packet to the client to terminate its side of the connection.

    - **ACK**: The client acknowledges the server's FIN packet with an ACK.  
        