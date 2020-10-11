## Solidity

* External Vs Public - External is for external only calls, public is for both external and internal calls (More gas)

### Function inputs

* Functions cannot accept maps and dynamic multi-dimensional arrays as inputs

### Function Types

* pure - cannot read or write from state or anything for the blocks
* view - cannot write to state or change anything for the blocks

### Modifiers

Modifiers can simply a function by moving shared code into a same part

```sol
contract Playground {    
    address public owner;
    
    constructor() public {
        owner = msg.sender;
    }
    
    modifier isOwner() {
        require(msg.sender == owner, 'is not owner');
        _;
    }
    
    modifier validateAddress(address _address) {
        require(_address != address(0), "Invalid Address");
        _;
    }
    
    function changeOwner(address _newOwner) public isOwner validateAddress(_newOwner) returns (bool val) {
        owner = _newOwner;
        
        val = true;
    }
}
```

### Global Variables

#### msg
  * msg.sender - the address executing the contract

#### block
  * block.timestamp - gets the timestap (uint in seconds)

### Inheritance

"is" is the keyword for inheritance

```sol
contract Playground {
    string public name = "Yang";
}

contract child is Playground {
    
}
```

** Mutli inheritance**

Below, B's methods will override's A's
order of A,B is based on that B should be more sophisticated than A (B might inherit more than A)
```sol
contract C is A, B {
    
}
```

### Visibility

* private - only accessible by the contract
* Internal - only accessible by the contract and child contracts
* public - accessible by all
* external - only use on methods and can only be called by other contracts/accounts


