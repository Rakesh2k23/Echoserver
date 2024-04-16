# Ethical-Hacking-Techniques---19CS417-
Ethicka Hacking Techniques - 19CS417 
```
RAKESH KUMAR.S
212221040137
CSE (III)
```
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
### SERVER CODE
```
#echo-server.py
import socket
HOST = "127.0.0.1"  # Standard loopback interface address (localhost)
PORT = 65432  # Port to listen on (non-privileged ports are > 1023)
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
### CLIENT CODE
```
# echo-client.py
import socket
HOST = "127.0.0.1"  # The server's hostname or IP address
PORT = 65432  # The port used by the server
with socket.socket(socket.AF_INET, socket.SOCK_STREAM) as s:
    s.connect((HOST, PORT))
    s.sendall(b"Hello, world")
    data = s.recv(1024)
print(f"Received {data!r}")
```
## OUTPUT:
### SERVER OUTPUT
![Screenshot 2024-03-22 133658](https://github.com/Rakesh2k23/ETHICAL_HACKING/assets/141472158/cba29cc7-8873-4d9a-a81b-bcec1ba2c105)

### CLIENT OUTPUT
![Screenshot 2024-03-22 133705](https://github.com/Rakesh2k23/ETHICAL_HACKING/assets/141472158/f4340d01-5e3d-41be-9012-c439cdf3f373)


## RESULT:
The program is executed successfully
