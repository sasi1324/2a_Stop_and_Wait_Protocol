# 2a_Stop_and_Wait_Protocol
NAME:RAJAMANIKANDAN R
REG NO:212223220082
## AIM: 
To write a python program to perform stop and wait protocol
## ALGORITHM:
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM:
## CLIENT:
```
import socket
s=socket.socket()
s.bind(('localhost',8000))
s.listen(5)
c,addr=s.accept()
while True:
 i=input("Enter a data: ")
 c.send(i.encode())
 ack=c.recv(1024).decode()
 if ack:
   print(ack)
   continue
 else:
   c.close()
   break
```
## SERVER:
```
   import socket
s=socket.socket()
s.connect(('localhost',8000))
while True:
 print(s.recv(1024).decode())
 s.send("Acknowledgement Recived".encode())
```
## OUTPUT:
## CLIENT:
![image](https://github.com/rajamanikandanravikumar/2a_Stop_and_Wait_Protocol/assets/145742839/6841bf36-fd34-4007-8b1e-accf3f526c3c)
## SERVER:
![image](https://github.com/rajamanikandanravikumar/2a_Stop_and_Wait_Protocol/assets/145742839/d8c89d83-b823-4953-89ff-4a7254d5d9c5)


## RESULT
Thus,python program to perform stop and wait protocol was successfully executed Thus, python program to perform stop and wait protocol was successfully executed.
