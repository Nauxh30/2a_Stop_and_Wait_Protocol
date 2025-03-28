# 2a_Stop_and_Wait_Protocol
## NAME : NAUSHEEN FATHIMA A .
## REGISTER NUMBER : 212224230179.
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
CLIENT:
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
SERVER:
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    print(s.recv(1024).decode()) 
    s.send("Acknowledgement Recived".encode())
```

## OUTPUT
CLIENT:
![cn1](https://github.com/user-attachments/assets/d1ff437f-76d9-4b78-8ff4-5165fec1fafb)

SERVER:
![cn1 2](https://github.com/user-attachments/assets/d610f71f-532c-4fe6-a274-69f0ecf480a4)


## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
