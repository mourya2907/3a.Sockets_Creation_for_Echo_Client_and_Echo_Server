# EX.NO:3a.CREATION FOR ECHO CLIENT AND ECHO SERVER USING TCP SOCKETS

# AIM
To write a python program for creating Echo Client and Echo Server using TCP
Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server .
4. Send and receive the message using the send function in socket.
## PROGRAM
## client.py
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```

## server.py
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
    ClientMessage=c.recv(1024).decode()
    c.send(ClientMessage.encode())
```
## OUPUT
## client.py
<img width="406" height="280" alt="Screenshot 2025-10-27 161855" src="https://github.com/user-attachments/assets/88fa3bb6-c9f1-4ee7-b451-912b63ff33b6" />

## server.py
 <img width="439" height="166" alt="Screenshot 2025-10-27 161832" src="https://github.com/user-attachments/assets/46260c85-7dc7-4543-bdcb-e1f96a3fdab5" />

## RESULT
Thus, the python program for creating Echo Client and Echo Server using TCP Sockets Links 
was successfully created and executed.
