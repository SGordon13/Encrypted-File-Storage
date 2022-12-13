Encrypted-File-Storage
Scott Gordon

This program was developed as the course project for COMP 5610.

STRUCTURE:
A standard text file is encrypted using AES 128-bit encryption.<br>
The encrypted file is then sent via socket communication to the server.<br>
The server stores the encrypted file.<br>
The user requests the file back by filename.<br>
The server sends the file back to the user.<br>
The user can decrypt the file using AES 128-bit decryption.<br>

The work here is built off of the AES implementation provided by Cecelia Wisniewska.<br>
The original work can be found here: https://github.com/ceceww/aes<br>

We are also providing a funcioning RSA demo as a part of our submission.<br>
The original goal was to encorperate this into our project, but we could not
get the pieces working together due to some issues.<br>
We still believe the effort we put into the RSA demo was worth submitting as
its own example.<br>


COMPILATION INSTRUCTIONS:
-copy the entire directory onto your local machine<br>
-open terminal and change the directory to the folder containing the source code<br>
-open a second terminal to the same location to serve as the server.<br>
-any files you wish to encrypt or store should be in the folder './data/client/'.<br>
-run these commands to cmopile each of the source code files:<br>
&ensp;g++ client.cpp -o ./client  <br>
&ensp;g++ server.cpp -o ./server  <br>
&ensp;g++ ./aes/encrypt.cpp -o ./aes/encrypt  <br>
&ensp;g++ ./aes/decrypt.cpp -o ./aes/decrypt  <br>
&ensp;g++ ./rsaDemo/rsaDemo.cpp -o ./rsaDemo/rsaDemo  <br>
  
RUNNING INSTRUCTIONS:  <br>
-run these commands and follow given instructions to run the program  <br>
-when prompted for file names, it is assumed the file is in './data/client/'.  <br>
-you must run the server before you run the client  <br>
    on client terminal: ./aes/encrypt  <br>
        enter the name of the file you wish to encrypt.  <br>
        resulting filename will have 'ENC' prepended.  <br>
    on server terminal: ./server  <br>
    on client terminal: ./client  <br>
        choose to upload file, then enter file name of the encrypted file.  <br>
    you may delete the file form the client folder.  <br>
        on server terminal: ./server  <br>
    on client terminal: ./client  <br>
        choose to download file, then enter file name of the encrypted file.  <br>
    on client terminal: ./aes/decrypt  <br>
        enter the name of the encrypted file to decrypt.  <br>
        resulting filename will remove the 'ENC' prepend.  <br>
