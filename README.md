# Piano
Mus
import java.util.HashMap;
import java.util.Map;
import java.util.Scanner;

class MusicalPiano {
    private Map<Character, String> noteMappings;

    public MusicalPiano() {
        noteMappings = new HashMap<>();
        noteMappings.put('a', "C");
        noteMappings.put('s', "D");
        noteMappings.put('d', "E");
        noteMappings.put('f', "F");
        noteMappings.put('g', "G");
        noteMappings.put('h', "A");
        noteMappings.put('j', "B");
    }

    public void playNote(String note) {
        System.out.println("Playing " + note + " note.");
        // Simulate playing the note (you can use a library to generate actual sound)
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        MusicalPiano piano = new MusicalPiano();

        System.out.println("Welcome to the Musical Piano!");
        System.out.println("Use the following keys to play notes:");
        System.out.println("a s d f g h j");

        while (true) {
            char keyPressed = scanner.next().charAt(0);
            if (piano.noteMappings.containsKey(keyPressed)) {
                String note = piano.noteMappings.get(keyPressed);
                piano.playNote(note);
            } else {
                System.out.println("Invalid key. Please use a s d f g h j.");
            }
        }
    }
}
