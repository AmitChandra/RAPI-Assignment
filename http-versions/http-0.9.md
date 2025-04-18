# Introduction

HTTP/0.9 was created in 1991 by Tim Berners-Lee — the inventor of the World Wide Web — as the very first version of the Hypertext Transfer Protocol. It was designed to be extremely simple to meet the needs of the earliest web browsers and servers. HTTP/0.9 was the first version of HTTP. It was extremely simple — it supported only one method: GET, and returned only raw HTML content, with no headers or metadata.

# Example request:

GET /index.html

# Context at the time:

- The web was just starting out.
- Web pages were purely static HTML documents.
- No images, no CSS, no JavaScript — just plain hypertext with links.
- The priority was simplicity and proof-of-concept communication between a browser and a web server.

# How it worked:

- The client (browser) would send a single-line GET request.
  Example: GET /index.html
- The server would respond with raw HTML content, with no HTTP headers, status codes, or metadata.
- The connection would close immediately after sending the response.
  It was essentially a one-way conversation — no back-and-forth negotiation, no additional information exchanged.

# Advantages of HTTP/0.9:

- Simplicity: Extremely easy to implement — just send a GET request and get back raw HTML.
- Low overhead: No headers, no metadata, only content — making it very lightweight.
- Fast for basic tasks: Because of its simplicity and no extra data, it was quick for very small,
  static HTML pages.

# Disadvantages (leading to HTTP/1.0 and then HTTP/1.1):

- No headers: No way to send metadata like content type, status codes, caching info, or connection
  control.
- Limited to GET: No support for other methods like POST, PUT, or DELETE, limiting interaction.
- Only raw HTML: Couldn’t transfer images, JSON, CSS, etc.
- No persistent connections: A new connection was needed for every request, adding significant
  overhead for multiple files on a page.
- No status codes: Couldn’t communicate error messages or response status — servers just sent raw
  data.
