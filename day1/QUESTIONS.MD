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
R: The function is missing the return and argument value Type, and the function tries to change a value on a let variable when let variables are immutables.
