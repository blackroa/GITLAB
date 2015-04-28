For User who have Visual Studio 10 or newer version installed(Windows User)

Getting Start (vistual Studio user)
---------------------------------------------------------

Starting File Transfer Server
---
1. Server is located in ConsoleApplication2 folder.
2. Open ConsoleApplication2.sln (Microsoft Visual Studio Solution File).
3. Press F5 to run the server program.
4. Go to Start.
5. Open command line.
6. Type ipconfig -> hit Enter
7. Find Server computer Ip address 
8. Find where the program call TcpListener() function and edit IP and port (in case server and client are run 
in the same computer default Ip Address is 127.0.0.1)
	8.1 in case your server ip address is 10.53.104.3 and port you wanted to use is 6969
		the code must be edit to "TcpListener serverSocket = new TcpListener(IPAddress.Parse("10.53.104.3"), 8000);"



---

Starting File Transfer Client
---
1. Client is located in ConsoleApplication3 folder0
2. Open ConsoleApplication3.sln (Microsoft Visual Studio Solution File).
3. Edit Server Ip address and port in main function where the code call client.Connect().
4. Use Ip address from "7th step of starting File Transfer Server" (default is set to 127.0.0.1 with port 8000)
	4.1 In case your Server Ip addres is 10.53.104.3 and you want to use port 6969
		the code must be edit to : "client.Connect("10.53.104.3", 6969);"
5. Press F5 to run the Client program.
6. Now the File transfering system is ready to use.
--

Note***
 Local(client) directory is located at "/ConsoleApplication3/bin/Debug"
 Remote(server) directory is located at "/ConsoleApplication2/bin/Debug"