# 2a_Stop_and_Wait_Protocol
## AIM 
To write a python program to perform stop and wait protocol
## ALGORITHM
1. Start the program.
2. Get the frame size from the user
3. To create the frame based on the user request.
4. To send frames to server from the client side.
5. If your frames reach the server it will send ACK signal to client
6. Stop the Program
## PROGRAM
## client:
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
##  server:
import socket\n
s=socket.socket()\n
s.connect(('localhost',8000))\n
while True:\n
 print(s.recv(1024).decode())\n
 s.send("Acknowledgement Recived".encode())\n
## OUTPUT
![image](https://github.com/MuthulakshmiD/2a_Stop_and_Wait_Protocol/assets/144870775/5b27486c-3fdf-4717-93e1-99d0140790ff)

## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
