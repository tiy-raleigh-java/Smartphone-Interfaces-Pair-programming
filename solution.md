```java
public class Smartphone implements AudioPlayer, Camera, Phone, Comparable<Smartphone> {

    private String brand;

    private int phoneNumber;

    private int totalPictures;

    private boolean playingMusic;

    private int volumeLevel;

    public void sendText() {
        System.out.println("Hey!");
    }

    public void takePicture() {
        totalPictures += 1;
    }

    public void playSong() {
        playingMusic = true;
    }

    public void receiveText() {
        System.out.println("How are you?");
    }

    public void zoomIn() {
      System.out.println("zooming out");
    }

    public void stopSong() {
        playingMusic = false;
    }

    public void zoomOut() {
        System.out.println("zooming in");
    }

    public void makePhoneCall() {
        System.out.println("calling 867-5309");
    }

    public void flash() {
        System.out.println("ouch my eyes");
    }

    public void volumeUp() {
        volumeLevel += 1;
    }

    public void volumeDown() {
        volumeLevel -= 1;
    }

    public int compareTo (Smartphone otherPhone) {
        //Whoever is loudest wins!
        if (this.volumeLevel > otherPhone.volumeLevel) {
            return 1;
        } else if (this.volumeLevel < otherPhone.volumeLevel) {
            return -1;
        }
        return 0;
    }
}
```

Interface:

```java
public interface AudioPlayer {

    public void playSong();

    public void stopSong();

    public void volumeUp();

    public void volumeDown();
}
```

Interface:

```java
public interface Camera {

    public void takePicture();

    public void zoomIn();

    public void zoomOut();

    public void flash();
}
```

Interface:

```java
public interface Phone {

    public void sendText();

    public void receiveText();

    public void makePhoneCall();
}
```
