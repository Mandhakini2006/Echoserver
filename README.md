# Echoserver
Echo server and client using python socket

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

Design of echo server and client using python socket

### Step 2:

Implementation using Python code

### Step 3:

Testing the server and client 

## PROGRAM:
client
```
import socket
HOST = "127.0.0.1" 
PORT = 65432  
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"NAME : MANDHAKINI A REG NO:212223100030")
    data = s.recv(1024)
print(f"Received {data!r}")
```
server
```
import socket
HOST = "127.0.0.1" 
PORT = 65432 
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.bind((HOST, PORT))
    s.listen()
    conn, addr = s.accept()
    with conn:
        print(f"Connected by {addr}")
        while True:
            data = conn.recv(1024)
            if not data:
                break
            conn.sendall(data)

```

## OUTPUT:
<img width="1919" height="552" alt="image" src="https://github.com/user-attachments/assets/9d1d7290-0484-472a-9cf9-2292de0daa80" />


## RESULT:
The program is executed successfully
