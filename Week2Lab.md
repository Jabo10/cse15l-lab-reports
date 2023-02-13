# Lab Report 2 - Servers and Bugs (Week 3) 
# Part 1 
This is the code for `StringServer.java` which is basically just a modified version of the exact same given code from `NumberServer.java`
```
import java.io.IOException;
import java.net.URI;
import java.util.ArrayList;

class Handler implements URLHandler {
    // The one bit of state on the server: an arraylist that will be manipulated by
    // various requests.
    // using basically the exact replica code but for strings and implimenting stringbuilder in order to print the contents properly with a space 
    ArrayList<String> al = new ArrayList<String>(); 
    
    public String handleRequest(URI url) {
        if (url.getPath().equals("/")) {
            return al.toString(); 
        } else {
            if (url.getPath().contains("/add-messages")) {
                String[] parameters = url.getQuery().split("=");
                String addedString = parameters[1]; 
                al.add(addedString); 
                if (parameters[0].equals("s")) {
                  StringBuilder builder = new StringBuilder();
                  for (String s : al) {
                      builder.append(s);
                      builder.append("\n"); 
                  }
                  String text = builder.toString(); 
                  return text; 
                    }
                }

                }
            
            return "404 Not Found!";
        }
    }

class StringServer {
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
**First Screenshot of using add-message**
![image](https://user-images.githubusercontent.com/122490992/215363679-92772149-ae0a-475f-8044-0d3ca79a5047.png)
**Second Screenshot of using add-message**
![image](https://user-images.githubusercontent.com/122490992/215363896-a7314e02-da55-4085-adc1-7f91a014099d.png)
 * What is first called for each screenshot from main method is Server.java in order to create the server 
 * Then `HandleRequest` is called from this `StringServer` where is handles the path of add-messages and adds each accordingly 
 * Within this method there are other calls to other java methods such as `getPath` which is a method that returns the path component of the URL, which is    the part of the URL after the domain name. 
 * As well as `getQuery` that returns the query string component of the URL, which is the part of the URL that follows the path and starts with a ?          character
 * `split` is also used to separate a string into an array of substrings based on a specified delimiters.
 * The relevant arguements are the URIs given as the url to those methods which dictate what will be displayed 
 * If the values were changed so would the output, for instance this code was changed to handle strings but it was orginally for ints given it it is from    `NumberServer`, and the value was switched from add to add-messages, as well as num to s, If no values were changed output would stay the same. 
 * In this case the array was empty to start with as there was no values/strings and when adding a message the array will go up by one as it holds each      entry. With this it outputs the entire list of strings with the help of the toString method which is a string representation. 
 * Overall it parses the query string for the s parameter, which should contain a string to be added to the al ArrayList. The method then adds the new        string to the end of the al ArrayList using the add method.

# Part 2
One of the bugs from lab 3 was given from `ArrayExamples.java` and it is the method `reversed` given as 
```
  // Returns a *new* array with all the elements of the input array in reversed
  // order
  static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }

```
Which would fail for this test that I wrote for in `ArrayTest.java` as a JUnit

```
@Test
  public void testReversed() {
    int[] input1 = { 1 , 2, 3 , 4 };
    assertArrayEquals(new int[]{ 4, 3 ,2, 1}, ArrayExamples.reversed(input1));
  }
```
The original test that did not produce a failure in JUnit was 
```
@Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```
These two Screenshots being the symptoms 
<img width="858" alt="image" src="https://user-images.githubusercontent.com/122490992/215367506-8d321976-49d5-463d-9041-779d5d03bbaa.png">

<img width="629" alt="image" src="https://user-images.githubusercontent.com/122490992/215367460-095b1116-8ca0-4099-8b6a-34c39febbf5f.png">
 
I then completely rewrote the code in a way that I saw fit becuase the reason why the orginal code had a bug was because the new array was empty meaning that the old array was being replaced by something with elements being only zeros. The reason that it fails the test case is because it does not reverse properly it only fills with zeros and does not return a new array at all, but it passed the empty array test because its implementation would work for the empty array being that it returns that original array without doing anything to it (does not enter for loop), an empty array reversed is still an empty array. So I decided to change this by making the new array hold the elements of the old array going in reverse then making the old array equal to the new array then returning it as such, 
 
 ```
 static int[] reversed(int[] arr) {
   int[] newArray = new int[arr.length];
   int k = 0;
   for(int i = arr.length - 1; i >= 0; --i) {
     newArray[k] = arr[i];
     ++k; 
   }
   arr = newArray;
   return arr;
  }
 ```
It is purposefully more than two codes in markdown because I prefer this version 

# Part 3
I learned just how easy it is to make a simple psuedoserver. I had no prior knowledge about the intricacies when it came to server side anything, so it was great to learn how to make a server both locally and remotely and also how to manipute its output through paths in the search bar. I also found it interesting how the ports worked and what it meant to connect to certain ones that others might also be using.    
