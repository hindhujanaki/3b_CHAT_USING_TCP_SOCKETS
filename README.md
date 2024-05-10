# 3b.CREATION FOR CHAT USING TCP SOCKETS
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
## Client
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
## Server:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode())
```
## OUPUT
## Client
![image](https://github.com/hindhujanaki/3b_CHAT_USING_TCP_SOCKETS/assets/148514666/e33474de-da1d-4664-91a5-710c29624d5e)

## Server:
![image](https://github.com/hindhujanaki/3b_CHAT_USING_TCP_SOCKETS/assets/148514666/a3b19be8-8be5-4b1d-9dc9-afcdbe89bb77)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
