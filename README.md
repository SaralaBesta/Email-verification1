# Email-verification1

package com.example.phase1;
import java.util.ArrayList;
import java.util.Arrays;
import java.util.List;
import java.util.Scanner;
public class EmailVerification {
	
	String array[]={"samba993@gmail.com","rohitsharma99@hotmail.com","viratkohli1999@yahoo.in","m.s.dhoni123@mail.com","saralabesta9@gmail.com","balaji2018@gmail.com",
			"archanabesta.2018@email.in","kanemawa@mail.org","alexpatels@gmail.com","renukaferari3@yahoo.in"};
	List<String> nameList = new ArrayList<>(Arrays.asList(array));
	Scanner sc=new Scanner(System.in);
	String s;
	
	public void entermail()
	{
		System.out.println("Enter an email for searching:");
		s=sc.next();
		System.out.println("entered an email::"+s);
	}
	public void emailvalidation(){
		int ind=nameList.indexOf(s);
		
		if(nameList.contains(s)==true)
		{
			System.out.println("USER AUTHENTICATED ::"+s);
			System.out.println("YOUR ENTERED EMAIL ID:"+ind);
		}
		else
		{
			System.out.println("UNAUTHORISED ACESS::"+s);
		}
	}
	public static void main(String[] args) {
		Scanner sc=new Scanner(System.in);
		EmailVerification obj=new EmailVerification();
		int n;
		
		while(true)
		{
			System.out.println("menu for mail search::");
			System.out.println("\n 1.Email enter for authentication");
			
			System.out.println("Enter your choice:");
			n=sc.nextInt();
			if(n==1)
			{
				obj.entermail();
			}
			else if(n==2)
			{
				obj.emailvalidation();
			}
			else
			{
				System.out.println("Exit");
				break;
			}
		}

	}

}

