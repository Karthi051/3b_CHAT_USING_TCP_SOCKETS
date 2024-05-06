# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM:
## CLIENT.PY:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
## SERVER.PY:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUPUT:
## CLIENT.PY:

![image](https://github.com/dinesh2068/3b_CHAT_USING_TCP_SOCKETS/assets/151390189/6340ccc8-50de-45f2-811a-b628716bc6e8)

## SERVER.PY:

![image](https://github.com/dinesh2068/3b_CHAT_USING_TCP_SOCKETS/assets/151390189/2a62d972-8df1-4b99-a7e2-fc17daef4930)

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
