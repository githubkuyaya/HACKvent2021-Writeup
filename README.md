# Notes for SuperSmartSanta.pdf:
The line

> *be careful to submit 100 wei to the contract, as this is wanted value in the original contract.*

is **incorrect**. It doesn't matter what value you submit, it will **always** be true (please correct me if I'm wrong).
The idea behind it, is that if the contract's original value (100) is subtracted by the contract's current value (e.g. 200), it will cause an integer overflow, as the type of `i` is `uint256`. It cannot be negative and will result in `2**256 - 100` (in our case here).
