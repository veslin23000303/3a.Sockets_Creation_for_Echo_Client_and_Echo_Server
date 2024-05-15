# 3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS
## NAME:VESLIN ANISH A
## REGISTER NO:212223240175
# AIM:
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM:
### CLIENT SIDE:
```python
import socket
s=socket.socket()
s.connect(('localhost',90))
while True:
 msg=input("Client > ")
 s.send(msg.encode())
 print("Server > ",s.recv(1024).decode())
```

### SERVER SIDE:
```python
import socket
s=socket.socket()
s.bind(('localhost',90))
s.listen(5)
c,addr=s.accept()
while True:
 ClientMessage=c.recv(1024).decode()
 c.send(ClientMessage.encode())
```

## OUPUT:

### CLIENT SIDE:

![Screenshot 2024-05-15 101752](https://github.com/veslin23000303/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/151148539/397c84da-353d-404a-91da-079ed0ddb755)


### SERVER SIDE:

![Screenshot 2024-05-15 101808](https://github.com/veslin23000303/3a.Sockets_Creation_for_Echo_Client_and_Echo_Server/assets/151148539/1ad46dc4-f248-4ad7-83ed-b4a2d2530ef9)


## RESULT:
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
