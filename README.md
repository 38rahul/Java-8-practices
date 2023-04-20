# Java-8-practices


/******************************************************************************

Welcome to GDB Online.
GDB online is an online compiler and debugger tool for C, C++, Python, Java, PHP, Ruby, Perl,
C#, OCaml, VB, Swift, Pascal, Fortran, Haskell, Objective-C, Assembly, HTML, CSS, JS, SQLite, Prolog.
Code, Compile, Run and Debug online from anywhere in world.

*******************************************************************************/
import java.util.*;
public class Main
{
// 	public static void main(String[] args) {
	
// 		System.out.println("Hello World");
// 		List<Integer> Number = List.of(1,50,7,9,0,99,87,100,20);
// 		List<String> Courses = List.of("Spring","Spring Boot","Api","Microservices","AWS","PCP","Azure","Docker","Kubernetes");
		
// 		for(Integer i: Number){
// 		    System.out.println(i+" ");
// 		}
		
// 		System.out.println("-------------printAllNumbers---------------");
// 		printAllNumbers(Number);
// 		System.out.println("-------------printEvenNumbers---------------");
// 		printEvenNumbers(Number);
// 		System.out.println("-------------printOddNumbers--------------");
// 		printOddNumbers(Number);
// 		System.out.println("-------------printAllCourses------------------");
// 		printAllCourses(Courses);
// 		System.out.println("-------------Contains Spring------------------");
// 		printAllCoursesContainsSpring(Courses);
		
// 		System.out.println("-------------print Courses whose length is greater than 4------------------");
// 		printAllCoursesLenthGreaterThan4(Courses);
		
// 		System.out.println("-------------Squares of Each Number------------------");
// 		printSquaresofAllNumbers(Number);
		
// 	}
// 	public static void printAllNumbers(List<Integer> Number){
// 	    Number.stream().forEach(System.out::println);
// 	}
// 	public static void printEvenNumbers(List<Integer> Number){
// 	    Number.stream().filter(i->i%2==0).forEach(System.out::println);
// 	}
//     public static void printOddNumbers(List<Integer> Number){
//         Number.stream().filter(i->i%2!=0).forEach(System.out::println);
//     }
//     public static void printAllCourses(List<String> Courses){
//         Courses.stream().forEach(System.out::println);
//     }
//     public static void printAllCoursesContainsSpring(List<String> Courses){
//         Courses.stream().filter(i->i.contains("Spring")).forEach(System.out::println);
//     }
    
//     public static void printAllCoursesLenthGreaterThan4(List<String> Courses){
//         Courses.stream().filter(i->i.length()>4).forEach(System.out::println);
//     }
//     public static void printSquaresofAllNumbers(List<Integer> Number){
//         Number.stream().map(num->num*num).forEach(System.out::println);


//             Playing with Streams

	public static void main(String[] args) {

	    List<Integer> Number = List.of(1,50,7,9,0,99,87,100,20);
	    System.out.println(addListStructured(Number));
	    System.out.println(addListFunctional(Number));
    }
    
    public static int addListStructured(List<Integer> Number){
       
       int sum=0;
        for(Integer num: Number){
            sum += num;
        }
        return sum;
    }
    // public static int sum(int aggegate, int nextnumber){
    //     System.out.println(aggegate+" "+ nextnumber);
    //     return aggegate + nextnumber;
    // }
    
     public static int addListFunctional(List<Integer> Number){
       
       int sum=0;
        //return Number.stream().reduce(0,Main:: sum);
       // return Number.stream().reduce(0,(x,y) -> x+y);
       return Number.stream().reduce(0,Integer:: sum);
    }


}
