Exception handling
======================
if code has exception error the application will stop running. (N.b. web app will redirect to a default error page.) When code has error an exception objct is created and works backwards through the code to find the point in the code that cn handle the exception.

You need to handle the exception to prevent the user experiencing this eror and to stop the application from crashing.

1. run code in debug
2. add a try/catch block to the code

```
try {
  DoSomething();
  }
  catch (exception err) {
  Console.riteLine("Error has occurred");
  }
  ```

catch exception - enables access to the exception error message.  used to log errors, retry what has failed. N.b it is not mandatory to have any code in the catch block.

N.b. adding throw; to the catch block it will continue moving upwards

returning 0 indicates success and any other number indicates fail.

The base class of every exception is exception. 

You can add finally block after try catch for code that will always execute even if there is an exception.
