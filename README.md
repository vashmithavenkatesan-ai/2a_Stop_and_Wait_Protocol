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
```
Client 
#Developed:VASHMITHA V
#Register no:212225240180

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

server:
```
#Developed:VASHMITHA V
#Register no:212225240180
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    print(s.recv(1024).decode()) 
    s.send("Acknowledgement Recived".encode())
```
## OUTPUT
client
<img width="637" height="791" alt="Screenshot 2026-05-21 133320" src="https://github.com/user-attachments/assets/d4dbd8d4-0572-4711-81e8-c8ccab79f02a" />



server

<img width="622" height="797" alt="Screenshot 2026-05-21 133349" src="https://github.com/user-attachments/assets/046a6754-f12e-407c-9a9e-9b91f28d5011" />



## RESULT
Thus, python program to perform stop and wait protocol was successfully executed.
