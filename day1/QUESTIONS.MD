1. How much is the current memory capacity of a canister?

R: 48gb


2. What is the issue with the following code sample?
```
actor {
  let counter : Nat = 0;
  public func increment_counter() : async () {
    counter := counter + 1;
  };
}
```
R: The function is missing the return value Type and the async declarations is without parenthesis, and the function tries to change a value on a let variable when let variables are immutables.


3. What is the issue with the following code sample?
```
actor {
  var message : Text = 0;

  public query func change_message(new_message : Text) : async () {
    message := new_message;
    return;
  };
  
  public query func see_message() : async Text {
    return(message);
  };
}
```
R: The variable message is declared how to type Text but the value is type Int, the function 'change_message' is missing the Type of the return value and the async declarations is without parenthesis, the function is missing the return value, and the function 'see_mesage' has an incorrect syntax for the return value, this value is declared without parenthesis. 


4. False or True: we can remove the keyword async for the return argument of a query function since queries are faster to answer.

R: False, you can't remove the async declaration for async functions, if you do this your function doesn't work correctly.
