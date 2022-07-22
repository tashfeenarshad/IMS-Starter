Coverage: 67%
# IMS

This IMS programme is designed to allow a usef to Create,read,update or delete a customer,item or order from the system.
## Getting Started

To begin using the project download a clone of the git repository of ims_project above, Here you can find a .jar file which can run the project via the command line or powershell. If you wish to make additions to the project clone to respository to your machine and run your prefered Java IDE (preferably Eclipse). Once you have eclipse open, go into your workspace and open "Open Project"
### Prerequisites

What things you need to install the software and how to install them
Java 8
MySQl 1.7 or greater
Maven
```
Give examples
```

### Installing

A step by step series of examples that tell you how to get a development env running

Say what the step will be

```
Give the example
```

And repeat

```
until finished
```

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system. Break down into which tests and what they do

### Unit Tests 

The JUnit tests in the program can be located in the src/test/java folder and are used in the DAO and domain classes, this contains code which tests out the variables and minor functionality which has be set up and uses fixed data to test

```
Give an example
public class ItemDAOtest {

	private final ItemsDAO DAO = new ItemsDAO();

	@Before
	public void setup() {
		DBUtils.connect();
		DBUtils.getInstance().init("src/test/resources/sql-Itemsschema.sql", "src/test/resources/sql-Itemsdata.sql");
	}

	@Test
	public void testCreate() {
		final Items created = new Items(2L, "choclate", 20.99);
		assertEquals(created, DAO.create(created));
	}


### Integration Tests 
The Integration tests in the program can be located in the src/test/java folder and are used in the Controller classes, this tests the object functions within your code

```
Give an example
@Test
	public void testCreate() {
		final String F_NAME = "barry", L_NAME = "scott";
		final Customer created = new Customer(F_NAME, L_NAME);

		Mockito.when(utils.getString()).thenReturn(F_NAME, L_NAME);
		Mockito.when(dao.create(created)).thenReturn(created);

		assertEquals(created, controller.create());

		Mockito.verify(utils, Mockito.times(2)).getString();
		Mockito.verify(dao, Mockito.times(1)).create(created);
	}


Explain what these tests test and why

```
Give an example
```

## Deployment

To run your .jar file for your project move into the command line or terminal(for Mac), move to the file location for your .jar file and enter

java -jar 'file'.jar
This will then run your test on your system and open your up to the first class of your project which is the runner and it will ask you for login details

## Built With

* [Maven](https://maven.apache.org/) - Dependency Management

## Versioning

We use [SemVer](http://semver.org/) for versioning.

## Authors

*Jordan Belbenbalid
*Piers Barber

## License

This project is licensed under the MIT license - see the [LICENSE.md](LICENSE.md) file for details 

*For help in [Choosing a license](https://choosealicense.com/)*

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
