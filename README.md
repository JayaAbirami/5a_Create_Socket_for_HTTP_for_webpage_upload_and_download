# 5a_Create_Socket_for_HTTP_for_webpage_upload_and_download
## AIM :
To write a PYTHON program for socket for HTTP for web page upload and download
## Algorithm

1.Start the program.
<BR>
2.Get the frame size from the user
<BR>
3.To create the frame based on the user request.
<BR>
4.To send frames to server from the client side.
<BR>
5.If your frames reach the server it will send ACK signal to client otherwise it will send NACK signal to client.
<BR>
6.Stop the program
<BR>
## Program 
## CLIENT
```
import socket 
s=socket.socket() 
s.connect(('localhost',8000)) 
while True: 
    msg=input("Client > ") 
    s.send(msg.encode()) 
    print("Server > ",s.recv(1024).decode()) 
```
## SERVER
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

## OUTPUT
## CLIENT
![image](https://github.com/JayaAbirami/5a_Create_Socket_for_HTTP_for_webpage_upload_and_download/assets/151487010/2d1f0405-c6de-42ad-8f19-eb6b028ba5a2)

## SERVER
![image](https://github.com/JayaAbirami/5a_Create_Socket_for_HTTP_for_webpage_upload_and_download/assets/151487010/bb849df4-7cd4-4d21-b555-0d1543e9a149)

## Result
Thus the socket for HTTP for web page upload and download created and Executed
