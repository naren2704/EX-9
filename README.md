## APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER
## EXP: 9
## DATE:03-05-2023
## AIM:
To write a python program for creating Chat using TCP Sockets Links.

## ALGORITHM:
## Client:
Import the necessary modules in python Create a socket connection to using the socket module. Send message to the client and receive the message from the client using the Socket module in server Send and receive the message using the send function in socket. 
## PROGRAM:

## CLIENT:
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
   ```
## SERVER:
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
## CLIENT OUTPUT :
![image](https://github.com/naren2704/EX-9/assets/118706984/5de642b0-cbbb-40e1-b4b9-ea479c546b54)
## SEVER OUTPUT:
![image](https://github.com/naren2704/EX-9/assets/118706984/f1059344-fe8f-4952-af8a-626160e2def4)
## RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.
