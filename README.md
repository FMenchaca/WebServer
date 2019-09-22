# WebServer

Modification to be done:

Read webserver.c to learn how it works. Specifically, look how webserver sends out the HTML document and from where to read it. Move the HTML document which is stored in string constant HOME_PAGE to a file called index.html in a directory you choose as the root directory of your directory tree where you put your documents; and modify webserver.c so that it reads HTML document from index.html when the client send a request with path /. (your server must know where to find the index.html file). Use a web browser to check your web server works.

Note: An HTTP request is composed of 3 parts: a web address, ex., www.uhd.edu; an application (or port) number, ex., 8080 (the default port number is 80); and a path of a file, ex., /faculty/yuans/misc.html. If no file name is given in the path, by default index.html or index.htm will be requested. For example, in URL http://www.uhd.edu:8080/facility/ computers.html, the web address is: www.uhd.edu, the port number is 8080; and the path is /facility/computers.html.

Activity 7: Replace the content of index.html file with HTML document for another web page. Use a web browser to get that page.

Activity 8: Add functionality to the web server so that it can handle a request for an arbitrary file.
This activity allows students learn how the web server handles a client request for an arbitrary file. So far, we have built a server which can only handle a request for the default web page “index.html” with path “/”. Generally, a web client can require for any file with a long path, e.g., the following URLs require “resume.html” and “/doc/manual.html”:

http://www.somewhere.com/resume.html

http://www.somewhere.com/doc/manual.html

In this activity, students need to modify the webserver.c program to handle the request with arbitrary file name. It will check the existence of the requested file. If no such file exists, it will send a “No file found” message to the client; otherwise, it will send the requested file to the client.

Step 1: Modify the webserver.c source code so that it can handle requests with any path as described above.

Step 2: Put index.html file in the root directory of your directory tree as you have done in Activity 6. Put other files in your directory tree and insert links in your index.html file to point to those files. Use a web browser to connect to the webserver with path “/”. The web page contained in “index.html” should appear in the browser. Then, click on the links in the webpage. Successive pages should appear. Look at the path in the URL window. You should see that files contained in the subdirectories should be requested.

Hint: You may want to study the following file I/O functions and use them in your program: fopen(), fseek(),ftell(), rewind(), fread(), fclose().
