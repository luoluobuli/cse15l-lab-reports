# Lab Report 2
## Part 1
CharServer.java
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    ArrayList<String> arr = new ArrayList<>();

    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return "";
        } else if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("&");
            String[] s = parameters[0].split("=");
            String[] user = parameters[1].split("=");
            if (s[0].equals("s") && user[0].equals("user")) {
                String addedLine = user[1] + ": " + s[1] + "\n";
                arr.add(addedLine);
                return String.join("", arr);
            }
        }
        return "Invalid input.";
    } 
}

class CharServer {
    public static void main(String[] args) throws IOException {
        if(args.length == 0){
            System.out.println("Missing port number! Try any number between 1024 to 49151");
            return;
        }

        int port = Integer.parseInt(args[0]);

        Server.start(port, new Handler());
    }
}
```

Screenshot 1
