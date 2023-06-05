## APPLICATION USING TCP SOCKETS - CREATING ECHO CLIENT-SERVER
## EXP : 8
## DATE : 27-04-2023
## AIM :
To write a python program for creating Echo Client and Echo Server using TCP Sockets Links.

## ALGORITHM :
```
1.Import the necessary modules in python
2.Create a socket connection to using the socket module.
3.Send message to the client and receive the message from the client using the Socket module in server.
4.Send and receive the message using the send function in socket.
```
## PROGRAM :
## CLIENT :
```python
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
   msg=input("Client > ")
   s.send(msg.encode())
   print("Server > ",s.recv(1024).decode())
```   
## SERVER :
```python
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
   ClientMessage=c.recv(1024).decode()
   c.send(ClientMessage.encode())
```   
## CLIENT OUTPUT :
![ex 8 cl output](https://github.com/MrSanthosh-dev/EX-8/assets/117916573/e8d38e94-5ee6-4206-858c-ccb581b096b5)


## SERVER OUTPUT :
![ex 8 se output](https://github.com/MrSanthosh-dev/EX-8/assets/117916573/e06a232f-ce6d-494f-9d63-7bcef733b356)


## RESULT :
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links was successfully created and executed.
