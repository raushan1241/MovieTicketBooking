import java.util.Scanner;

class MovieTicketBooking {
    static Scanner sc = new Scanner(System.in);
    static String[] movieList = { "1)Avatar", "2)Robot 2.0", "3)Transformer", "4)Avenger", "5)Ice age" };

    public static void main(String[] args) {
        try {
            User user = new User();
            user.login();
            getname();
        } catch (Exception e) {
            System.out.println("An error occurred: " + e.getMessage());
        }
    }

    public static void getname() throws Exception {
        String name;
        System.out.println("Enter your name:");
        name = sc.nextLine();
        if (name.isEmpty()) {
            throw new Exception("Name cannot be empty");
        }
        System.out.println("WELCOME " + name);
        getmovie();
    }

    public static void getmovie() throws Exception {
        System.out.println("Select the movie from the list:");
        for (int i = 0; i < movieList.length; i++) {
            System.out.println(movieList[i]);
        }
        int choice = sc.nextInt();
        if (choice < 1 || choice > 5) {
            throw new Exception("Invalid movie selection");
        }
        System.out.println("You selected: " + movieList[choice - 1]);
        getseat();
    }

    public static void getseat() throws Exception {
        int n;
        System.out.println("How many seats do you want?");
        n = sc.nextInt();
        if (n <= 0) {
            throw new Exception("Number of seats must be positive");
        }
        int[] arr = new int[n];
        System.out.println("Choose your seats:");
        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }
        int amount = n * 150; // 1 ticket cost is 150
        System.out.println("Total amount to pay: " + amount);
        System.out.println("Please select your bank to pay:");
        System.out.println("1) Axis Bank");
        System.out.println("2) ICICI Bank");
        System.out.println("3) Indian Bank");
        System.out.println("4) State Bank");

        int bank = sc.nextInt();
        switch (bank) {
            case 1:
                System.out.println("Welcome to Axis bank");
                break;
            case 2:
                System.out.println("Welcome to ICICI bank");
                break;
            case 3:
                System.out.println("Welcome to Indian bank");
                break;
            case 4:
                System.out.println("Welcome to State bank");
                break;
            default:
                throw new Exception("Invalid bank selection");
        }
        System.out.println("Enter the amount:");
        int amountpay = sc.nextInt();
        if (amountpay == amount) {
            System.out.println("Your payment is successfully completed.");
            System.out.println("Your seat has been successfully booked.");
            System.out.println("Thank you!");
        } else {
            throw new Exception("Payment amount does not match the total amount");
        }
    }
}

class User {
    private String username;
    private String password;

    public void login() throws Exception {
        System.out.println("Enter your username:");
        username = MovieTicketBooking.sc.nextLine();
        if (username.isEmpty()) {
            throw new Exception("Username cannot be empty");
        }

        System.out.println("Enter your password:");
        password = MovieTicketBooking.sc.nextLine();
        if (password.isEmpty()) {
            throw new Exception("Password cannot be empty");
        }
    }
}
