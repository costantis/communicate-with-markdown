# Header
## 
###
#### 

![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)
``` java
public class Main {

	private static ApplicationContext ctx;

	public static void main(String[] args) throws PerformanceException {
		ctx = new ClassPathXmlApplicationContext(
				new String[] {
						"com/springinaction/springidol/concrete/performers/performers.xml",
						"com/springinaction/springidol/concrete/instruments/instruments.xml",
						"com/springinaction/springidol/concrete/poems/poems.xml", });

		Performer performer = (Performer) ctx.getBean("carl");
		performer.perform();
	}

}
```
