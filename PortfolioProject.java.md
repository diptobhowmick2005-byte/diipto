#   
import java.util.*;  
  
class Project {  
    String name;  
    String tech;  
  
    Project(String name, String tech) {  
        this.name = name;  
        this.tech = tech;  
    }  
  
    void display() {  
        System.out.println("Project: " + name + " | Tech: " + tech);  
    }  
}  
  
public class PortfolioProject {  
    public static void main(String[] args) {  
        Scanner sc = new Scanner(System.in);  
        ArrayList<Project> projects = new ArrayList<>();  
  
        while (true) {  
            System.out.println("\n1. Add Project");  
            System.out.println("2. View Projects");  
            System.out.println("3. Exit");  
            System.out.print("Choose: ");  
  
            int choice = sc.nextInt();  
            sc.nextLine();  
  
            if (choice == 1) {  
                System.out.print("Enter Project Name: ");  
                String name = sc.nextLine();  
  
                System.out.print("Enter Technology: ");  
                String tech = sc.nextLine();  
  
                projects.add(new Project(name, tech));  
                System.out.println("Project Added!");  
            }  
  
            else if (choice == 2) {  
                for (Project p : projects) {  
                    p.display();  
                }  
            }  
  
            else {  
                break;  
            }  
        }  
  
        sc.close();  
    }  
}  
