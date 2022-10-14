# Lab Report 2
## Part 1
**Code for Search Engine**
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {

    ArrayList<String> lst = new ArrayList<String>();
    String output = "";
    public String handleRequest(URI url) {
        if (url.getPath().contains("/add")) {
            String query = url.getQuery();
            String strToAdd = query.substring(2);
            lst.add(strToAdd);
        }
        else if (url.getPath().contains("/search")) {
            String query = url.getQuery();
            String strToSearch = query.substring(2);
            for (int i = 0; i < lst.size(); i++) {
                if (lst.get(i).contains(strToSearch)) {
                    output = output + " " + lst.get(i);
                }
            }
            return output;
        }
        return "";
    }
}

class SearchEngine {
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

**Adding a new string**
![]