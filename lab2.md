# Ned Bitar's Lab Report 2.
##### This lab report will be broken down into three sections:

##### - Part 1: Web Server

##### - Part 2: Debugging

##### - Part 3: Things learned from week 2 or 3.
<br>

## Part 1: WebServer
This is a piece of software written by me, that simply<br>
takes input from the URL bar and then displays it for the user.<br>
My implementation specifically keeps track of the input, and displays <br>
it at once.
<br><br>
Here is the code for this:
<br>
```java
private static String cannedURL = "add-message";

    public String handleRequest(URI url) {
        
        if (url.getPath().contains(cannedURL)) {
            parameters = url.getPath().split("=");
            this.history = this.history + parameters[1] + "\n";
            return history;
        }
        return "not it chief";
}


class NumberServer {
    public static void main(String[] args) throws IOException {
        if(args.length != 0) {
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }
        int port = 25565;//Integer.parseInt(args[0]);
        Server.start(port, new Handler());
    }
}
```
### Screenshot showing StringServer Usage:
#### Screenshot: 1
![image](1photo/joeB.png)
<br><br>

My code follows the ethos of simplicity. Once the path is changed, my method, handleRequest is called.
It then goes and checks to see if the path contains the cannedURL, if it does, it looks for what is 
after the "=" sign, and then it appends it to the history string. This history string is then returned
to the user.
<br><br>#### Screenshot: 2
![image](1photo/hotdogw.png)
<br><br>

The code consists of two classes, Handler and NumberServer. The Handler class implements the handleRequest method, which is called when the URL path is changed. The method checks if the URL path contains the string stored in the cannedURL variable, which is "add-message". If the URL path does contain the string, the method splits the path using "=" as a separator, and appends the resulting value to the history string. The updated history string is then returned to the user.

The NumberServer class sets up a server with a specified port number. If no port number is provided in the command line arguments, it defaults to 25565. The start method of the Server class is called with the specified port number and an instance of the Handler class, allowing the handleRequest method to handle incoming requests.
## Part 2: Debugging
