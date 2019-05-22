## Networking Assignment [100 points + 35 EC]

Deliverable: Answers to questions & C++/Python programs.

# Background Reading

## The Browser Question [10 points]

Here's a common interview question:

```
What happens when you type google.com into your browser's address box and press enter?
```

[The answer's nontrivial](https://github.com/alex/what-happens-when). 

**[Reading 1] Skim the table of contents & vaguely google/wikipedia & grok the words.**

**Question 1a: Provide a valid HTTP/1.1 request header & some interesting commentary about it. [10 points]**

**[EC] Question 1b: Why is the content-length header of a HTTP response important? [10 points]**

## Beej's Guide to Network Programming [40 points]

[Beej's Guide to Network Programming](http://beej.us/guide/bgnet/html/multi/index.html) is a classic.

**[Reading 2] Read the table of contents. Read Section 2 (What is a Socket?), 3 (IP Addresses), 5 (System Calls or Bust)**.

**Question 2a: What's a socket? What's the difference between TCP and UDP? [10 points]**

**Question 2b: Describe the parameters to socket(). What does it return? [10 points]**

**Question 2c: What do bind, listen, and accept do on a server? What does connect do for a client? [10 points]**

**Question 2d: What's the difference between send/recv and sendto/recvfrom? Why are the arguments different? Connect this with your answer to Q1. [10 points]**

# Project: Chatroom. [50 points]

Implement 4 simple chatrooms in Python and C++.

Ensure your C++ & Python TCP chatrooms can cross-communicate. Likewise with the UDP chatrooms. [10 points]

Program 1 - TCP & Python [10 points]
- Reference https://www.geeksforgeeks.org/simple-chat-room-using-python to implement a TCP-based chatroom in python.

Program 2 - TCP & C/C++ [10 points]
- Port your TCP python chat server to C++.

Program 3 - UDP & Python [10 points]
- Reference https://tutorialedge.net/python/udp-client-server-python/ to implement a UDP-based chatroom in python.

Program 4 - TCP & C/C++ [10 points]
- Port your UDP python chat server to C++.

## Extra Credit

Support multiple TCP clients per chatroom. [10 points]  
Support multiple UDP clients per chatroom. [5 points]  
