# EX-8 APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER

## DATE : 24/04/23

## AIM :
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.

## ALGORITHM :
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
 .
4. Send and receive the message using the send function in socket.

## PROGRAM :
### client :
```python
Developed by : Tejusve Kabeer.F
Register no : 212222100054

import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
### Server :
```python
Developed by : Tejusve Kabeer.F
Register no : 212222100054

import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```

## OUTPUT :

### clientoutput:
![5co](https://github.com/Reebak04/EX-8/assets/118364993/789db051-e99b-4088-b733-c871cc46bb1f)

### serveroutput:
![so](https://github.com/Reebak04/EX-8/assets/118364993/79af8b63-a6ab-436d-9899-724a1d5d27a2)

## RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links
was successfully created and executed.
