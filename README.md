# 3b.CREATION FOR CHAT USING TCP SOCKETS
## Name:Sanjev R M
## REG NO:212223040186
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
### CLIENT
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
### SERVER
```python
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
## OUPUT
### CLIENT
![image](https://github.com/sanjevrm/3b_CHAT_USING_TCP_SOCKETS/assets/155142423/694002df-bdf8-4445-9f88-8e349e62f62b)


### SERVER
![image](https://github.com/sanjevrm/3b_CHAT_USING_TCP_SOCKETS/assets/155142423/0b2d0a4a-19fa-4857-841a-90959ebf73aa)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
