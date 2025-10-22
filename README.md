import java.util.ArrayList;
import java.util.Scanner;
public class Todolist{
    public static void main(String[]arrg){
        Scanner sc=new Scanner(System.in);
        ArrayList<String>tasks=new ArrayList<>();
        int choice;
        while(true){
            System.out.println("1.Add Task");
            System.out.println("2.Veiw Tasks");
            System.out.println("3.remove rtask");
            System.out.println("4.exit");
            System.out.print("enter your choice:");
            choice=sc.nextInt();
            sc.nextLine();
            switch(choice){
                case 1:
                System.out.print("enter new task:");
                String task=sc.nextLine();
                System.out.println("task added!");
            break;
            case 2 :{
            System.out.println("\nyour tasks:");
            if(tasks.isEmpty()){
                System.out .println("no task yet.");

            }else{
                for(int i=0;i<tasks.size();i++){
                    System.out.println((i+1)+"."+tasks.get(i));
                }
            }
        }break;
        case 3:{
        System.out.print("enter task number to remove:");
        int tasknum=sc.nextInt();
        if(tasknum>0 && tasknum<=tasks.size()){
            tasks.remove(tasknum-1);
            System.out.println("task removed!");
    }else{
        System.out.println("invalid task number.");
    }
}break;
case 4: 
System.out.println("exiting...");
sc.close();
return;
default:
System.out.println("invalid choice.please try again.");
            }
        }
    }
}
