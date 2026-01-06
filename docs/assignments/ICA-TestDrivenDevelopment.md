# Test Driven Development

This activity is an introduction to Test Driven Development using Java and JUnit tests.  The problem being solved is to create a Java class that can be used to represent a password.

## Setup

Follow the steps below to get setup for this activity:

1. Open a browser and log into your GitHub account.
2. Click the link below:
   - [https://github.com/codespaces/new/Dickinson-COMP-491-492/PasswordTDDExercise](https://github.com/codespaces/new/Dickinson-COMP-491-492/PasswordTDDExercise)

3. Click the Green "Create new codespace" button to create a Codespace using the starter project for the activity:

    ![Create new Codesapce](images/tdd/CreateCodespace.png)

This will open VSCode in your browser, but it will take a few minutes to complete.

4. When the files appear in the "EXPLORER" pane, click the `PasswordTest.java` file to open it.

5. Wait for the dialog about sharing data with Redhat to appear in the lower right corner.  Click Close or "Deny" this dialog dialog.  This may take a few moments.

6. Wait for the status bar at the bottom of the browser window to display:

   ![Java: Lightweight Mode](images/tdd/JavaLightweightMode.png)

7. Click the "Java: Lightweight Mode" area of the status bar.

8. That area of the status bar will change a few times and then eventually it will display:

   ![Java: Ready](images/tdd/JavaReady.png)

Once you see "Java: Ready" you are ready to go!

## Running the Test

The provided `PasswordTest.java` file contains a single JUnit test that checks if an instance of the `Password` class can be created. This is a reasonable first test for a TTD approach to our problem of creating a Java class to represent a password.

Run this test by:
1. Right click on the `PasswordTest.java` file in the "EXPLORER PANE"
2. Choose "Run Tests" from the pop-up menu.
3. When the tests run the "Test Runner for Java" panel should open in the lower right corner of the window.
   - If the "Test Runner for Java" panel doesn't open, click the "Tests Results" tab that appears at the top of the Terminal panel.

Observe that the test has failed with an "Unresolved Compilation" error.  This should not be too surprising since we haven't yet created the `Password` class.

## Making the Test Pass

To make the test pass you'll need to create the `Password` class.  

Create the `Password` class by:
1. Right click in the empty are of the EXPLORER panel.
2. Choose "New Java File" in the pop-up menu.
3. Choose "Class..." from the pop-up sub-menu.
4. Enter `Password` as the name for the new class.

Notice that a new `Password.java` file has been created and it contains the skeleton for the `Password` class.  This should be sufficient for the test that was failing to now pass.

Run the test in `PasswordTest.java` again and observe that it now passes.

## Next Steps

Now it's time to do some Test Driven Development.  

Consider the following requirements for the `Password` class:
- Each new password must:
  - be at least 8 characters long.
  - contain at least one digit.
  - contain at least one special character [#$%!?].
  - accept the desired password as an argument to the constructor.
  - set the password to `null` if it does not meet the criterion.

Practice TDD to implement the `Password` class by following the six steps illustrated in the flowchart below, which was adapted from Martin Fowler's short description of [Test Driven Development](https://martinfowler.com/bliki/TestDrivenDevelopment.html):

[<center><img src="images/tdd/tdd-flowchart.jpg" alt="Flowchart adapted from Martin Fowler's blog that illustrates the TDD process and the six steps described below." width="50%"/></center>](images/tdd/tdd-flowchart.png "TDD Flowchart")

1. Create a list of tests that you will use.
2. Pick a test to write.
3. Write and run a JUnit test for that test.
   - You may find this [list of JUnit Assertions with Examples](https://github.com/junit-team/junit4/wiki/Assertions) helpful.
   - Run the tests.
     - The old test(s) should still pass.
     - The new one should fail.
4. Write the code to implement the functionality being tested.
   - Remember, do the __minimum amount of work__ you can to do get the test to pass.
     - If you think you need to do more, define a new test and add it to your list.
     - Then still do the minimum amount of work for the test you are working on.
   - Run the tests and debug until all tests including the new test pass.
5. Do any refactoring to clean up and/or simplify the code.
   - Run the tests frequently during refactoring to ensure you have not broken anything.
6. If your list of tests is not empty, goto 2.

## Changing Requirements

If you have more time consider these additional requirements and then use TDD to implement some or all of them. Be sure to refactor your code as necessary after getting each new test to pass.

- The `Password` class must now:
  - provide a way to change the password
  - ensure that when a password is changed the new password meets the same constraints as a new password (above).
  - not allow any of the previous 5 passwords to be reused.


---

![Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png "Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License") All textual materials used in this course are licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](http://creativecommons.org/licenses/by-nc-sa/4.0/)

![GPL V3 or Later](https://www.gnu.org/graphics/gplv3-or-later-sm.png "GPL V3 or later") All executable code used in this course is licensed under the [GNU General Public License Version 3 or later](https://www.gnu.org/licenses/gpl.txt)
