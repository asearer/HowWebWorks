Part 1
- What is HTTP?
Hyper Text Transfer Protocol is governs how clients get data from, or send data to, a server.

- What is a URL?
Short for Uniform Resource Locator, a URL is an address for some internet resource.

- What is DNS?
Short for Domain Name System, this is a system that takes human-readable URLs and converts them into IP addresses.

- What is a query string?
The query string allows you to pass key-value pairs into the URL, in the format ?key1=value1&key2=value2...

- What are two HTTP verbs and how are they different?
GET - get some data from the server (most pages, search forms)
POST - send some data to the server (pages that change data on server)

- What is an HTTP request?
An HTTP request is a request from a client to a server which follows the HTTP protocol (eg a request for HTML from news.google.com)

- What is an HTTP response?
An HTTP request is a request from a client to a server which follows the HTTP protocol (eg a request for HTML from news.google.com)

- What is an HTTP header? Give a couple examples of request and response headers you have seen.
Headers provide additional information about the request or the response. Here are some examples:
Request headers: Host, User-Agent, Accept, Cookie, Cache-Control
Response headers: Content-Type, Last-Modified, Set-Cookie, Cache-Control

- What are the processes that happen when you type “http://somesite.com/some/page.html” into a browser?
1. Your browser “resolves” the name into an IP address using DNS
2. Your browser makes a request to that IP address, including headers (info about browser, any previous cookies, and other things)
3. The server sends a response (typically, HTML, with a status code (200 if it was sucessful)
4. The browser makes a DOM from that HTML, and finds any other resources needed (images, CSS, JavaScript, etc)
5. The browser makes a DOM from that HTML, and finds any other resources needed (images, CSS, JavaScript, etc)

Part 2
curl -H "Accept: application/json" "https://icanhazdadjoke.com/search?term=pirate"

{"current_page":1,"limit":20,"next_page":1,"previous_page":1,"results":[{"id":"QuscibaMClb","joke":"What does a pirate pay for his corn? A buccaneer!"},{"id":"SvzIBAQS0Dd","joke":"What did the pirate say on his 80th birthday? Aye Matey!"},{"id":"2gii3LeN7Ed","joke":"Why couldn't the kid see the pirate movie? Because it was rated arrr!"},{"id":"SnOf2gqjiqc","joke":"Why are pirates called pirates? Because they arrr!"},{"id":"exXSCtkOKe","joke":"Why do pirates not know the alphabet? They always get stuck at \"C\"."}],"search_term":"pirate","status":200,"total_jokes":5,"total_pages":1}

dig +short icanhazdadjoke.com

104.21.66.15
172.67.198.173

Part 3
PS C:\Users\amsea\Desktop\HowWebWorks> python3 -m http.server
Serving HTTP on :: port 8000 (http://[::]:8000/) ...
::ffff:127.0.0.1 - - [13/Jul/2023 09:17:59] "GET / HTTP/1.1" 200 -
::ffff:127.0.0.1 - - [13/Jul/2023 09:17:59] code 404, message File not found
::ffff:127.0.0.1 - - [13/Jul/2023 09:17:59] "GET /favicon.ico HTTP/1.1" 404 -





