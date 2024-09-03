---
date: 2024-09-02T13:17:27-04:00
title: 'A URL Journey'
draft: false
description: 'What happens when you type a URL into a browser?'
featured_image: '/images/AdobeStock_822553479_Preview.jpeg'
tags: [web, networking]
---

I was recently asked, "What happens when you type a URL into your browser?" It's a question that always makes me pause, trying to gauge the right level of detail. This time, I clearly missed the mark. In hindsight, I should have asked some clarifying questions to better understand the depth of knowledge the person was seeking. It's a lesson I know well, but sometimes, in the heat of the moment, even the simplest things can trip us up.

Inspired by this experience, I decided to dive deep into the answer myself. This article is the culmination of that research. So, the next time someone asks you the same question, you'll be ready to give a thorough response – after asking the appropriate clarifying questions, of course!

## Browser Processing
### Identify URL Componenets
The browser will parse the URL to identify its different components:
- Scheme
- Hostname
- Port
- Path
- Query Parameters
- Fragment

### DNS Lookup
The browser needs the IP addess of the server associated with the hostname. 
- the browser checks it's local cache first.
- if the IP addess is not in the cache, it queries a recursive DNS resolver. 
- [//]: # (- TODO add more depth here.)

### Establishing a TCP Connection
- 3 way handshake


### Sending a HTTP Request
- Request Line
- headers
- Body

### Server Processing and Responses

### Browser Rendering
