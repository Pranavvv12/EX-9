# EX-9 APPLICATION USING TCP SOCKETS - CREATING FOR CHAT CLIENT-SERVER
# EXP: 9
## DATE:03-05-2023
### AIM:
To write a python program for creating Chat using TCP Sockets Links.

### ALGORITHM:
## Client:
1.Import the necessary modules in python
2.Create a socket connection to using the socket module.
3.Send message to the client and receive the message from the client using the Socket module in server
4.Send and receive the message using the send function in socket.
### PROGRAM:
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
![image](https://github.com/Pranavvv12/EX-9/assets/121292280/2fd2b419-50f6-429e-9277-17eaac3567b0)


## SERVER OUTPUT :
![image](https://github.com/Pranavvv12/EX-9/assets/121292280/6adc89c6-76ca-47f0-a2ba-180852b7ddab)


### RESULT:
Thus, the python program for creating Chat using TCP Sockets Links was successfully created and executed.

