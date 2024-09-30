- Text based protocol
- [TCP](https://www.fortinet.com/resources/cyberglossary/tcp-ip) for transport
- URLs
- Stateless
- Request and response
- Headers and Body
- Defined in [RFC 2626](https://www.ietf.org/rfc/rfc2626.txt)
	- Updated in RFCs 7230,7233,7234,7235 (2015)

Request Methods

- GET: Visit a link
- POST: submit a form
- PUT: create a resource 
- PATCH: update a resource
- DELETE: delete a resource
- TRACE: echo the request
	- When you get back the echo request and its different than what you sent out that means there's something between you and the server
- CONNECT: establish a tunnel to target (e.g. proxy)
- OPTIONS: list supported verbs

Response codes
1. 100-series: informational
2. 200-series: OK
3. 300-series: redirects
	- 301,302 Moved (permanent, temporary)
	- 304 Not Moved
4. 400-series: bad client
	- 400 bad request
	- 401 Unauthorized
	- 403 Forbidden
	- 404 Not Found
5. 500-series: bad server
	- 500 internal server error
	- 502 bad gateway
	- 503 Service unavailable

HTTP 2.0
HTTP/2: RFC7540 (in 2015)
Performance improvements
	Multiplexing: concurrent streams address "head of line blocking"
	devs can assign priority and dependencies for resources
	Header
"Speculative server push"
	PUSH_PROMISE frame
TCP and encrypted connections only (user-agent decision)

HTTP 3
is HTTP-over-QUIC
Quick UDP internet connections
QUIC replaces TCP and TLS
	encryption is required
	QUIC: RFC 9000 (May 2021)
	HTTP/3 is a draft (July, 2021)

HTTP version doesn't matter *
Differences are at the transport layer

Fundamental problems with browsers
- Download random code
- from random places
- run it immediately
- prevent dangerous operations
- keep sites separate from each other
- but don't be too strict
- quickly
- don't inconvenience anyone

fundamental solution: same origin policy
- resource from same origin can fully interact with each other
- resources from different origins a re restricted
	- can send request, not read response
- Origin = (scheme + host + port)
- origin = (protocol + domain name + port)
- CORS is a way to selectively violate the Same-Origin Policy
	- api.twitter.com can fully interact with twitter.com

XML
	- Text
	- tags <h1>
	- attribute <h1 name="attribute">
	 - replaced elements <img>
Usually contains not HTML bits
- javascript
- CSS
- SVG
- Inline images

Rendering
several passes of tokenizing and parsing
tokenizing: identifying "words"
	lexical analysis or lexing
