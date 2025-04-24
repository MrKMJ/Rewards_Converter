# Rewards Converter
This is the project repo for the JPMC Software Engineering Lite Program, consult the program instructions for more information.
This Java project provides a utility to convert between cash values and airline miles.

## Files

* `RewardValue.java`: This file contains the `RewardValue` class, which handles the conversion logic between cash and miles. It has constructors to create `RewardValue` objects from either cash or miles, and methods to retrieve the cash or miles value. The conversion rate used is 0.0035 (1 mile = $0.0035).

* `RewardValueTests.java`: This file contains JUnit tests for the `RewardValue` class. It includes tests to verify the correct creation of `RewardValue` objects with cash and mile values, as well as tests to ensure the accuracy of the cash-to-miles and miles-to-cash conversions.

* `RewardsConverter.java`: This file contains the `RewardsConverter` application, which takes a cash value as input from the user and displays the equivalent value in airline miles.

## How to Use

1.  **Compile the Java files:**
    ```bash
    javac RewardValue.java RewardValueTests.java RewardsConverter.java
    ```

2.  **Run the RewardsConverter application:**
    ```bash
    java RewardsConverter
    ```

3.  The application will prompt you to enter a cash value. After you enter the value, it will display the equivalent number of airline miles.

## Testing

To run the JUnit tests, you need to have JUnit 5 installed. You can then compile and run the tests from the command line or use an IDE like IntelliJ IDEA or Eclipse.

**Command line example:**

1.  **Compile the test files with the JUnit 5 libraries:**
    ```bash
    javac -classpath ".:/path/to/junit-jupiter-api-5.x.x.jar:/path/to/junit-jupiter-engine-5.x.x.jar:/path/to/opentest4j-1.x.x.jar" RewardValueTests.java
    ```
    (Replace `/path/to/...` with the actual paths to your JUnit 5 JAR files.)

2.  **Run the tests:**
    ```bash
    java -classpath ".:/path/to/junit-jupiter-api-5.x.x.jar:/path/to/junit-jupiter-engine-5.x.x.jar:/path/to/opentest4j-1.x.x.jar:/path/to/apiguardian-1.x.x.jar;org.junit.platform.commons-1.x.x.jar;org.junit.platform.engine-1.x.x.jar;org.junit.platform.launcher-1.x.x.jar;org.junit.platform.reporting-1.x.x.jar" org.junit.platform.console.ConsoleLauncher --class-path . --scan-classpath --select-class=RewardValueTests
    ```
    (Again, replace `/path/to/...` with the actual paths.)

## Class Details

### `RewardValue`

* **Fields:**
    * `cashValue`:  A `double` representing the cash value.
    * `milesValue`: A `double` representing the equivalent value in miles.
    * `MILES_TO_CASH_RATE`: A `static final double` constant defining the conversion rate (0.0035).

* **Constructors:**
    * `RewardValue(double cashValue)`:  Initializes a `RewardValue` object with the given cash value and calculates the corresponding miles value.
    * `RewardValue(int milesValue)`: Initializes a `RewardValue` object with the given miles value and calculates the corresponding cash value.

* **Methods:**
    * `getCashValue()`: Returns the cash value.
    * `getMilesValue()`: Returns the miles value.

### `RewardsConverter`

* This class contains the `main` method, which provides a command-line interface for the user to convert cash to miles.  It takes user input and uses the `RewardValue` class to perform the conversion.
