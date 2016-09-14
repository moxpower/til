# Asynchronous programming

Asynchronous programming enhances overall responsiveness
When a function has the `async` decorator, the compiler knows that the method contains an `await` statement.

From [MS docu](https://msdn.microsoft.com/en-us/library/mt674882.aspx):

> Asynchrony is essential for activities that are potentially blocking, such as when your application accesses the web. Access to a web resource sometimes is slow or delayed. If such an activity is blocked within a synchronous process, the entire application must wait. In an asynchronous process, the application can continue with other work that doesn't depend on the web resource until the potentially blocking task finishes.

Here is an example:

```C#
public static async void Method()
{
	await Task.Run(new Action(LongTask));
	Console.WriteLine("New Thread");
}
```