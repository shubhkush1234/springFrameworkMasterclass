In28minutes/spring-master-class

1. Introduction to spring-master-class
2. Spring framework in depth
3. Basic web app with Spring MVC
4. Introduction to SpringBoot
5. Spring AOP and AspectJ
6. Spring JDBC and JPA with Hybernate
7. Basics of Eclipse, Maven, JUnit and Mockito

Typical code:
```
public class ComplexBusinessService {
	
	SortAlgorithm sortAlgo = new BubbleSortAlgorithm();

}
```
```
public class BubbleSortAlgorithm implements SortAlgorithm{
 . . . 
 }
 ```
 Here, ComplexBusinessService is directly creating instance of BubbleSortAlgorithm (dependancy). It's tight coupling.
 
 To remove tight coupling, we make use of a constructor,
``` 
public class ComplexBusinessService {
	
	SortAlgorithm sortAlgo; // = new BubbleSortAlgorithm();

	public ComplexBusinessService (SortAlgorithm sortAlgo){
	
		this.sortAlgo= sortAlgo;
}
```
```
public class BubbleSortAlgorithm implements SortAlgorithm{
	. . . 
	}
```	