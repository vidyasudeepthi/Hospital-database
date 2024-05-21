# Hospital-database
homework
Hospital database
person name age gender 
doctor speciallity
patient disease bedno
nurse roomno floor
person.java
package Hospital;

public class person {
	private String name;
	private int age;
	private String gender;
	public person(String a,int b, String c) {
		this.name=a;
		this.age=b;
		this.gender=c;
	}
	void personOutput() {
		System.out.println("name= " + this.name);
		System.out.println("age= " + this.age);
		System.out.println("gender= " + this.gender);
		
	}

}
doctor.java
package Hospital;

import Hospital.person;

public class doctor extends person {
	private String speciality;
	private String disease;
	private int bedno;
	private int roomno;
	private int floor;
	
	
	public doctor(String a,int b,String c,String t,String s,int v, int y,int x) {
		super(a,b,c);
		this.speciality=t;
		this.disease=s;
		this.bedno=v;
		this.roomno=y;
		this.floor=x;
	}
	void doctorOutput() {
		super.personOutput();
		System.out.println("doctor speciality = "+this.speciality);
		System.out.println("patient  disease = "+this.disease);
		System.out.println("patient  bedno = "+this.bedno);
		System.out.println("nurse  roomno = "+this.roomno);
		System.out.println("nurse  floor = "+this.floor);
	}

}

patient.java
package Hospital;
import Hospital.person;
public class patient extends person {
	private String disease;
	private String speciality;
	private int bedno;
	private int roomno;
	private int floor;
	public patient(String a,int b,String c,String t,String g,int v,int y,int x) {
		super(a,b,c);
		this.speciality=t;
		this.disease=g;
		this.bedno=v;
		this.roomno=y;
		this.floor=x;
		
		
	}
	void doctorOutput() {
		super.personOutput();
		System.out.println("doctor speciality = "+this.speciality);
		System.out.println("patient  disease = "+this.disease);
		System.out.println("patient  bedno = "+this.bedno);
		System.out.println("patient  roomno = "+this.roomno);
		System.out.println("patient  floor = "+this.floor);
		
	}

}

nurse.java
package Hospital;
import Hospital.person;
public class nurse extends person {
	private String disease;
	private String speciality;
	private int bedno;
	private int roomno;
	private int floor;
	
	public patient(String a,int b,String c,String t,String g,int v,int y,int x) {
		super(a,b,c,t,g,v,y,x);
		this.speciality=t;
		this.disease=g;
		this.bedno=v;
		this.roomno=y;
		this.floor=x;
		
		
	}
	void doctorOutput() {
		super.personOutput();
		System.out.println("doctor speciality = "+this.speciality);
		System.out.println("patient  disease = "+this.disease);
		System.out.println("patient  bedno = "+this.bedno);
		System.out.println("nurse  roomno = "+this.roomno);
		System.out.println("nurse  floor = "+this.floor);
		
	}

}

main.java
package Hospital;

import java.util.Scanner;

public class Main {
  public static void main(String[] args) {
	  Scanner sc=new Scanner(System.in);
	  System.out.println("Enter the person name");
	  String m=sc.next();
	  System.out.println("Enter the person age");
	  int p=sc.nextInt();
	  System.out.println("Enter the person gender");
	  String s=sc.next();
	  System.out.println("Enter the doctor speciality");
	  String t=sc.next();
	  System.out.println("Enter the patient disease");
	  String g=sc.next();
	  System.out.println("Enter the patient bedno");
	  int v=sc.nextInt();
	  System.out.println("Enter the nurse roomno");
	  int y=sc.nextInt();
	  System.out.println("Enter the nurse floor");
	  int x=sc.nextInt();
	  doctor d=new doctor(m,p,s,t,g,v,y,x);
	  d.doctorOutput();
	  
  }
}

Output:-
Enter the person name
sudee
Enter the person age
23
Enter the person gender
female
Enter the doctor speciality
eye
Enter the patient disease
infection
Enter the patient bedno
3
Enter the nurse roomno
5
Enter the nurse floor
2
name= sudee
age= 23
gender= female
doctor speciality = eye
patient  disease = infection
patient  bedno = 3
nurse  roomno = 5
nurse  floor = 2

	







