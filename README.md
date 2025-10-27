# EX.NO:3b.CREATION FOR CHAT USING TCP SOCKETS
# NAME - PRIYADARSHINI K
# REG NO - 212224100046
## AIM
To write a python program for creating Chat using TCP Sockets Links.
## ALGORITHM:
1. Import the necessary modules in python
2. Create a socket connection to using the socket module.
3. Send message to the client and receive the message from the client using the Socket module in
 server
4. Send and receive the message using the send function in socket.
## PROGRAM
# client.py
```
import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
    msg=input("Client > ")
    s.send(msg.encode())
    print("Server > ",s.recv(1024).decode())
```

# server.py
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

## OUPUT
# client.py
![WhatsApp Image 2025-10-27 at 23 35 35_76cc14e9](https://github.com/user-attachments/assets/69fae517-9598-4165-bb8e-9871a31289b5)

# server.py
![WhatsApp Image 2025-10-27 at 23 36 00_a2624b76](https://github.com/user-attachments/assets/a5be403e-8b45-4136-a78b-50824259bb3a)


## RESULT
Thus, the python program for creating Chat using TCP Sockets Links was successfully 
created and executed.
