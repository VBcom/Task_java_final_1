import java.util.*;

public class PhoneBook {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        HashMap<String, HashSet<String>> phoneBook = new HashMap<>();

        System.out.println("Введите имя и телефон через пробел (для выхода введите end):");
        while (true) {
            String input = scanner.nextLine();
            if (input.equals("end")) {
                break;
            }
            String[] splitInput = input.split(" ");
            String name = splitInput[0];
            String phone = splitInput[1];

            HashSet<String> phones = phoneBook.computeIfAbsent(name, k -> new HashSet<>());
            phones.add(phone);
        }

        List<Map.Entry<String, HashSet<String>>> entries = new ArrayList<>(phoneBook.entrySet());
        entries.sort((o1, o2) -> Integer.compare(o2.getValue().size(), o1.getValue().size()));

        for (Map.Entry<String, HashSet<String>> entry : entries) {
            System.out.println(entry.getKey() + ": " + entry.getValue());
        }
    }
}
