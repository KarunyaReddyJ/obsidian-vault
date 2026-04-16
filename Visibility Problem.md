This problem occurs in multi threaded programs when a thread modifies the shared variable while the other thread sees the stale value for sometime which could cause inconsistent behaviour of programs.

The core reasons for this problem are:
- CPU Caching: as modern CPUs have their own cache tier per core when a thread starts execution it might read the value from main memory and still the same old cache value of it while the other thread modifies.
- JIT compilers: They try to optimize code by reordering the instructions or caching the values in registers.