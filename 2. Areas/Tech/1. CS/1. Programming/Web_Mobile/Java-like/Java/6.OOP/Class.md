 #java #Structure   
```java
package Person;

  

public class Person {

    private String Name;

    private int Age;

    private String Sid;

    private String Address;

  
  

    public Person(){};

    public Person(String name){

        this.Name = name;

    }

    public Person(String name, int age){

        this.Name = name;

        this.Age = age;

    }

    public Person(String name, int age, String sid, String address){

        this.Name = name;

        this.Age = age;

        this.Sid = sid;

        this.Address = address;

        System.out.println(sid + "," +name + "," + age + "," +  address);

    }

  

    //Name

    public String getName(){

        return Name;

    }

    public void setName(String name){

        this.Name = name;

    }

  

    //Age

    public int getAge(){

        return Age;

    }

    public void setAge(int age){

        this.Age = age;

    }

  
  

    //Sid

    public String getSid(){

        return Sid;

    }

    public void setSid(String sid){

        this.Sid = sid;

    }

  
  

    //Address

    public String getAddress(){

        return Address;

    }

    public void setAddress(String address){

        this.Address = address;

    }

  
  

    public void show(){

        System.out.println(this.Name + "," + this.Age);

    }

}
```

## Extend
```java
package Person;

  

public class Student extends Person {

    //Variable

    private String Name;

    private int Age;

    private String Sid;

    private String Address;

  
  

    public Student(){};

    public Student(String name){

        this.Name = name;

    }

    public Student(String name, int age){

        this.Name = name;

        this.Age = age;

    }

    public Student(String name, int age, String sid, String address){

        this.Name = name;

        this.Age = age;

        this.Sid = sid;

        this.Address = address;

        System.out.println(sid + "," +name + "," + age + "," +  address);

    }

  

    public void Learn(){

        System.out.println("Learn");

    }

  

}
```