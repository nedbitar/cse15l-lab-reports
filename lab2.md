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
[!image] (1photo/joeB.png)

