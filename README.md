# ChatAppWindowsForms
Simple Chat application which works across two different IP addresses 

// This Chat Application works best when you are able to use a Toolbox designer in VS IDE in which you can play with the GUI

sck - Refers to the sockets which are related to a devices. It works as an inter-process communicator and seen as the endpoint of the process communication. For communication, the socket uses a file descriptor and is mainly employed in client-server applications. A socket consists of the IP address of a system and the port number of a program within the system. 

SetSocketOption - Sets the specified socket option to the specified value, represented as an object.

SocketType.Dgram - Requires no connection prior to sending and recieving data, and can communicate with multiple peers.

GetLocalIP(); - The procedure of the program to obtain the host's IP and your friends IP (this is obviously an out of context code snippet and textLocalIP.Text is an example of what can be intialised with GetLocalIP.

foreach - Executes a block of code on each element in an array or a collection of items. When executing foreach loop it traversing items in a collection or an array. The foreach loop is useful for traversing each items in an array or a collection of items and displayed one by one. 

Side Note:
When you have a connection there are general rules

1) You can only have one connection with the source IP address, destination IP addreess, and port number 

2) You can't have the same IP address for both the source and destination IP address 

3) You can't open the same port number twice with the same IP address. 

Here are the rules you should use for configurating your connection

1) Server 

Use an IPEndpoint with port 80 and IPAddressAny. Instead of using a socket you cna use a TCPListener(). The Listener is a 
little bit easier to configure, but there is nothing wrong with using a Socket.

2) Client 

Don't use any IPEndPoint. Instead just use the Connect method with the IP Address of the Server. Instead of Socket you can
use TCPClient which will automatically to all the required configuration settings. 

Note: Port 80 is not a good choice of port numbers to use becuase it may be used by another application and even blocked by a firewall or virus checker. For custom applications I always recommend using a port number abover 10,000 that other people would not pick. Something random. Don't pick a number that ends in zeros like 11000 or a pattern like 12345.

Convert.ToInt32(String) - Converts the specified string representation of a number to an equivalent 32-bit signed integer.

AsyncCallBack - is a delegate which represents a callback method that is called when the asynchronous operation completes. The callback method takes an IAsyncResult parameter, which is subsequently used to obtain the results of the asynchronous operation. 
