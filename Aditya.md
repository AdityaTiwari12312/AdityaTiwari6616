import java.util.*;

class Game
{
    public static void main()
    {
    
        System.out.println("\tWELCOME! IN THIS GAME YOU HAVE TO GUESS THE NUMBER");
        Random random=new Random();
        int a,b;
        boolean d=false;
        for (int v=0;v<=1000;v=v+200)
        {
                for (int u=0;u<=10;++u)
        {
        int x=v+200;
        System.out.println("\tHINT 1:The number is between 0 to "+x);
        int f=0;
        b=random.nextInt(x);
        int y=b%10;
        System.out.println("\t\t\tHINT 2:The number end with "+y);
        while(!d)
        {
            Scanner sc=new Scanner(System.in);
            System.out.print("Enter Your Guess:");
            a=sc.nextInt();
            f++;
            if (a>b)
            {
                System.out.println("Too High");
            }
            else if (a<b)
            {
                System.out.println("Too Low");
            }
            else
            {
                d=true;
                System.out.println("Congrotulation! You have selected the required number in :"+f+" Guess");
            }
        }
        d=false;
        if (f<=10)
        {
            System.out.println("\t\tCongrotulation! Level "+u+" COMPLETED \u263A");
        }
        else 
        {
            System.out.println("\t\tOpps! Level "+u+" Failed \u2639A");
        }  
        }
    }
}
}
