
## Question
You are developing a multimedia player application that can play different types of media files, including audio and video. Implement the Simple Factory design pattern to create a MediaPlayer class that can instantiate specific media player objects based on the type of media file (e.g., MP3 for audio, MP4 for video). Provide a class diagram and explain how the Simple Factory pattern simplifies the object creation process for different media types in your design.

In your answer, describe the roles and responsibilities of each class involved in the Simple Factory pattern and how it allows for easy extensibility when adding support for new media types in the future. Additionally, discuss any potential improvements or enhancements to this design pattern for handling additional features or formats.


## UML
![Screenshot 2023-09-05 at 6 14 32 PM](https://github.com/SiddharthMathurDeveloper/Backend-Engineering/assets/133037456/9e174808-e3f5-44e3-ba40-d21bfdc21140)



## Code

### Client.java
```java
public class Client {
    
    public static void main(String[] args) {
        Media media = MediaSimpleFactory.createMedia("Mp3");

        media.stop();
        media.goBackwards();
        media.play();
        media.fastForward();
        System.out.println("The address of the called class: " + media);
    }
    
}
```


### MediaSimpleFactory.java
```java
public class MediaSimpleFactory {
    
    public static Media createMedia(String type){

        return switch (type) {
            case "Mp3" -> new Mp3Media();
            case "Mp4" -> new Mp4Media();
            case "WAV" -> new WAVMedia();
            default -> throw new IllegalArgumentException("Invalid Media Type");
        };

    }

}
```


### Media.java
```java
public interface Media {
     void play();

     void stop();

     void fastForward();

     void goBackwards();
}
```


### Mp3Media.java
```java
public class Mp3Media implements Media {
    @Override
    public void play() {
        System.out.println("Mp3 is started Playing");
    }

    @Override
    public void stop() {
        System.out.println("Mp3 is stopped");
    }

    @Override
    public void fastForward() {
        System.out.println("Mp3 fast forward by 5 seconds");
    }

    @Override
    public void goBackwards() {
        System.out.println("Mp3 went back by 5 seconds");
    }
}
```




### Mp4Media.java

```java
public class Mp4Media implements Media{
    @Override
    public void play() {
        System.out.println("Mp4 is started Playing");
    }

    @Override
    public void stop() {
        System.out.println("Mp4 is stopped");
    }

    @Override
    public void fastForward() {
        System.out.println("Mp4 fast forward by 5 seconds");
    }

    @Override
    public void goBackwards() {
        System.out.println("Mp4 went back by 5 seconds");
    }
}
```



### WAVMedia.java
```java
public class WAVMedia implements Media {
    @Override
    public void play() {
        System.out.println("WAV is started Playing");
    }

    @Override
    public void stop() {
        System.out.println("WAV is stopped");
    }

    @Override
    public void fastForward() {
        System.out.println("WAV fast forward by 5 seconds");
    }

    @Override
    public void goBackwards() {
        System.out.println("WAV went back by 5 seconds");
    }
}
```


















