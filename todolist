import java.util.ArrayList;
import java.util.Scanner;

public class TaskListApp {
    private ArrayList<String> taskList;     //define an arraylist
    private Scanner scanner = new Scanner(System.in);

    public TaskListApp() {
        taskList = new ArrayList<>();         //Create an arraylist to store tasks
    }

    public void start() {
        int choice = 1;

        do {
            System.out.println("\nTask List Application");
            System.out.println("1. Add Task");
            System.out.println("2. Remove Task");
            System.out.println("3. List Tasks");
            System.out.println("4. Exit");
            System.out.print("Enter your choice: ");

            choice = scanner.nextInt();
            scanner.nextLine(); // Consume the newline character

            switch (choice) {
                case 1:
                    addTask();
                    break;
                case 2:
                    removeTask();
                    break;
                case 3:
                    listTasks();
                    break;
                case 4:
                    System.out.println("Exiting the application. Goodbye!");
                    break;
                default:
                    System.out.println("Invalid choice. Please try again.");
            }
        } while (choice != 4);
    }

    private void addTask() {
        System.out.print("Enter the task: ");
        String task = scanner.nextLine();
        taskList.add(task);
        System.out.println("Task added successfully!");
    }

    private void removeTask() {
        if (taskList.isEmpty()) {
            System.out.println("Task list is empty. Nothing to remove.");
            return;
        }

        System.out.println("Current Tasks:");
        listTasks();

        System.out.print("Enter the task number to remove: ");
        int taskNumber = scanner.nextInt();
        scanner.nextLine(); // Consume the newline character

        if (taskNumber >= 1 && taskNumber <= taskList.size()) {
            String removedTask = taskList.remove(taskNumber - 1);
            System.out.println("Task '" + removedTask + "' removed successfully!");
        } else {
            System.out.println("Invalid task number. No task removed.");
        }
    }

    private void listTasks() {
        if (taskList.isEmpty()) {
            System.out.println("Task list is empty.");
        } else {
            System.out.println("Tasks:");
            for (int i = 0; i < taskList.size(); i++) {
                System.out.println((i + 1) + ". " + taskList.get(i));
            }
        }
    }

    public static void main(String[] args) {
        TaskListApp taskListApp = new TaskListApp();    //Create an instance of class TaskListApp
        taskListApp.start();
    }
}
