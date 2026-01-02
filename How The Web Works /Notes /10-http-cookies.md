
# HTTP Cookies

Date: 24/12/2025  
Topic: HTTP Fundamentals – Cookies

==================================================

WHAT ARE COOKIES?

Cookies are small pieces of data stored locally on the user's browser.
They are created when a web server sends a Set-Cookie header in an HTTP response.

Cookies exist because HTTP is a STATELESS protocol.
This means the server does not remember previous requests by default.

==================================================

WHY COOKIES EXIST

Without cookies:
- Every request is treated as a new user
- Login systems would not work
- User preferences would be lost

With cookies:
- The server can recognize returning users
- Sessions persist across requests
- Personalization becomes possible

==================================================

COOKIE LIFECYCLE (STEP BY STEP)

--------------------------------------------------
STEP 1: INITIAL REQUEST (NO COOKIE YET)

Client sends a request:

GET / HTTP/1.1
Host: cookies.example
User-Agent: browser-name

The browser has no stored cookie yet.

--------------------------------------------------
STEP 2: SERVER RESPONDS WITH A PAGE

Server response:

HTTP/1.1 200 OK
Content-Type: text/html

The server sends a webpage (for example, a form asking for a name).

--------------------------------------------------
STEP 3: CLIENT SENDS DATA (POST REQUEST)

Client submits form data:

POST / HTTP/1.1
Host: cookies.example
User-Agent: browser-name
Content-Type: application/x-www-form-urlencoded
Content-Length: 9

name=adam

--------------------------------------------------
STEP 4: SERVER SETS THE COOKIE

Server response:

HTTP/1.1 200 OK
Set-Cookie: name=adam
Content-Type: text/html

The browser stores the cookie locally.

--------------------------------------------------
STEP 5: FUTURE REQUESTS AUTOMATICALLY INCLUDE THE COOKIE

Client request:

GET / HTTP/1.1
Host: cookies.example
User-Agent: browser-name
Cookie: name=adam

The browser automatically sends the cookie on every request.

--------------------------------------------------
STEP 6: SERVER RECOGNIZES THE USER

Server response (HTML content):

<html>
  <body>Welcome back adam</body>
</html>

The server reads the cookie and responds with personalized content.

==================================================

WHAT COOKIES USUALLY STORE

- Session IDs
- Authentication tokens
- User identifiers

IMPORTANT:
Cookies do NOT store passwords.
They store random tokens linked to server-side data.

==================================================

COMMON USES OF COOKIES

- User authentication
- Session management
- User preferences
- Shopping carts
- Analytics and tracking

==================================================

VIEWING COOKIES IN THE BROWSER

Method 1 (Network):
1. Open Developer Tools
2. Go to the Network tab
3. Select a request
4. Open the Cookies section

Method 2 (Storage):
Application / Storage -> Cookies

==================================================

KEY SUMMARY

Cookies allow servers to remember users across multiple HTTP requests.
They solve the stateless nature of HTTP and enable modern web functionality.


https://youtu.be/s04Vjlcgwco
