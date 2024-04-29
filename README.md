# 3b.CREATION FOR CHAT USING TCP SOCKETS       
NAME:N.NAVYA SREE       
REG.NO:212223040138      
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
Client.py:
```
import socket
s=socket.socket()
s.connect(('localhost',800))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```
Server.py:
```
import socket
s=socket.socket()
s.bind(('localhost',800))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 print("Client > ",ClientMessage)
 msg=input("Server > ")
 c.send(msg.encode())
```
## OUPUT
Client Window:

![image](https://github.com/23004513/3b_CHAT_USING_TCP_SOCKETS/assets/138973069/8d4a99ca-72eb-4bae-bda7-64d6a9c2f644)

Server Window:

![image](https://github.com/23004513/3b_CHAT_USING_TCP_SOCKETS/assets/138973069/c8ea6702-098c-4748-8cf3-d580c73096b0)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
