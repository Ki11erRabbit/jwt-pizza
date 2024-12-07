# Formal Verification

Formal verification is a way of ensuring the correctness of the code.
Testing is only able to verify the existance of bugs. A test passing doesn't tell you much, you now know that there is no error for that particular case. While this might give you confidense in your code. However, you still don't know if a different value might break your code.

Formal verification seeks to use mathematics to check the correctness of code via one of these aproaches:
- model checking
- theorem proving
- abstract interpretation

All of these aproaches involve creating a mathematical model of the system at hand and proving properties about said model. This allows for much greater confidence in one's code as we can prove that there are not any bugs in the code we have written.

## Projects/companies that use Formal Verification

#### CompCert C Compiler
This is a verified C compiler. The team that developed it tested their compiler against other popular C compilers and found very few errors in the CompCert compiler but found many in popular compilers.

#### seL4 Kernel
seL4 is a operating system kernel that is written in C but verified using the Coq theorem proover. Their proofs show that the kernel is free of deadlocks, livelocks, buffer overflows, arithmetic exceptions, and uninitialized variables. These are all common issues in C code that can cause kernel panics.

#### Airbus
Airbus is a aviation company that uses formal verification in their software development stack. If their software breaks during a flight, it may cause the death of of hundreds of people at the minimum. With the growing use of embedded systems in planes, software bugs will only get worse as time goes on.

## Downsides
There are quite a few downsides to formal verfication which would explain why it isn't used in anything but the most critical software applications

#### Slow Development Time
It can be slow to formally prove the model of the software system. It can be hard to prove things about programs. Another cause is that if you make any changes to the code, you may have to completely rewrite the proof. In our world of 'move quick and break things,' companies would likely lose their first mover advantage and fall behind. As what happened to Plan 8 from Bell Labs, Good enough was the enemy to better.

#### Lack of Training
At least in the US, many developers and programmers have not be taught how to use formal verification to reduce errors in their code. This compounds with the above downside to create a chicken and egg problem where since there is little demand for formal verification, there are less people taught how to do it. It should also be noted that the above projects and companies all have origins in France which is also the origin country of the Coq theorem prover.

#### Proving the Wrong Model
It is very easy to prove a faulty model. If the model isn't correct, then you might as well have done nothing.


## Conclusion
Hopefully, formal verification becomes more popular as computers find their ways into everything and our lives. I believe that it can significantly reduce the amount of bugs in critical infrastructure that can save lives and money.

