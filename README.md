# Simple-FTP-Protocol
Simple FTP server and client using socket programming written in Python.

The client can upload files to the server or download files from the server.

## How To Run
Before Running the code,
Install python2 to exeute
In a terminal run the server.
```
cd server
python tcp_server.py
```
Then in a new terminal let the client ping the server.
```
cd client
python tcp_client.py
```

From here the client can send requests to the server

### Simple Commands

#### Simple Message Response
The server will respond to any message from the client by capitalization.
```
Message: hi
Received:  HI 
```
#### OPEN Port
The OPEN command will change the connection to the specified port number.
Input Command is `OPEN <port number>`

#### QUIT
Will quit out of the client connection. Client socket is closed and cannot connect to anything else, server is only left with welcome socket.
Command: `QUIT`

#### CLOSE
Similar to QUIT - Will close the connection between the client and the server, so the server is listening to receive connections and the client is free to make other connections.
Command: `CLOSE`

#### PUT
Will upload a file from the client directory to the server.
Command: `PUT <filename>`

#### GET
Will retrieve a file from the server and save it in the client directory.
Command: `GET <filename>`

#### LIST
Will retrieve a file lists all the files in the server directory.
Command: `LIST`
