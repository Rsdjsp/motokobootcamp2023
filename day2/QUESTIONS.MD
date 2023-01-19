1.Who controls the ledger canister?

R: The ledger of the NNS is ryjl3-tyaaa-aaaaa-aaaba-cai, and it is controlled by canister r7inp-6aaaa-aaaaa-aaabq-cai.


2.What is the subnet of the canister with the id: mwrha-maaaa-aaaab-qabqq-cai? How many nodes are running this subnet?

R: Canister subnet ID pae4o-o6dxf-xki7q-ezclx-znyd6-fnk6w-vkv5z-5lfwh-xym2i-otrrw-fqe. There is 16 node machines.


3.I have a neuron with 1O ICPs locked with a dissolve delay of 4 years - my neuron has been locked for 2 years. What is my expected voting power?

R: Approximately 14.2%. Additionally, an annualized voting reward of approximately 7.6%.

4.What is wrong with the following code?
```
actor {
  let n : Nat = 50;
  let t : Text = "Hello";

  public func convert_to_text(m : Nat) : async Text {
    Nat.toText(m);
  };
 
}

```
R: We need to import mo:base/Nat, also 'n' and 't' don't have any use


5.What is wrong with the following code?
```
actor {
  var languages : [var Text] = ["English", "German", "Chinese", "Japanese", "French"];

  public func show_languages(language : Text) : async [var Text] {
    return (languages);
  };
 
}

```
R: We need to delete the "var"  actor from the Array declaration and delete it again for the return value type

6.What is wrong with the following code?
```
actor {
  var languages : [Text] = ["English", "German", "Chinese", "Japanese", "French"];

  public func add_language(new_language: Text) : async [Text] {
    languages := Array.append<Text>(languages, [new_language]);
    return (languages);
  };
 
}

```
R: We need to import "mo:base/Array" and delete the 'return' actor


