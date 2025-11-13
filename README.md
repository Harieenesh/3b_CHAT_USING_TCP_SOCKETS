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
## SERVER:
```
import socket
s = socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr = s.accept()
while True:
    ClientMessage = c.recv(1024).decode()
    print("Client > ",ClientMessage)
    msg = input("Server > ")
    c.send(msg.encode())
```
## CLIENT:
```
import socket
s = socket.socket()
s.connect(('localhost',8000))
while True:
    msg = input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```
## OUPUT

<img width="1128" height="349" alt="Screenshot 2025-11-11 082755" src="https://github.com/user-attachments/assets/06024752-236f-457d-9435-177bd727e9c7" />

<img width="1103" height="342" alt="Screenshot 2025-11-11 082803" src="https://github.com/user-attachments/assets/b478a1f2-f730-483b-abc9-99d5a61935ac" />

## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
