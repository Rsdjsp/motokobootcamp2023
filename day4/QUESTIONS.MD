1. Is the heap memory saved when upgrading a canister? How much heap memory does a canister has?**

R: It will be saved only if the variable uses the stable keyword, if the variable type changes, the dApp could be broken.
The maximum heap memory is 4GB.

2. How much accounts can a unique Principal own?**

R: Almost a unlimited number of accounts can be created by a single Principal.

3. Can we safely upgrade a canister from interface A to interface B?**

R: Yes, it is possible to safely upgrade a canister from interface A to interface B, because the are not stored variables and the return type is the same.

Interface A

```motoko
actor {
  public func greet(surname : Text, firstname : Text) : async Text {
    return "Hello" # firstname # surname # " !";
  };
}
```

Interface B

```motoko
actor {
  public func greet(firstname : Text) : async Text {
    return "Hello" # firstname # " !";
  };
}
```