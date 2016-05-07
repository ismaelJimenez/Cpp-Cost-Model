# C++ Cost-Model

# C++ Running Time Analysis

The experiments are runned for inputs of various size, and then the running time is found by a least-squares fit to find the coefficient for the high order term. 

The machine used was an Intel(R) Core(TM) i5-3210M CPU @ 2.50GHz and 4GB RAM.

#### Cost of C++ Vector Operations
###### v1 and v2 are length-n std::vectors<int> and v3 is an empty vector
| Operation | Command | Running Time | Size | RMS error |
| --- | --- | --- | --- | --- |
| Create an empty vector | vector<int> v1 | less than 2 nanoseconds | N = 1 | 1% |
| Push back N items | v3.push_back(...) | 2.57084 * N nanoseconds | N <= 64000 | 13% |
| Find | find(v1.begin(), v1.end(), item) | 0.385456 * N nanoseconds | N <= 64000 | 18% |
| Access | v1.at(500) | less than 2 nanoseconds | N <= 64000 | 1% |
