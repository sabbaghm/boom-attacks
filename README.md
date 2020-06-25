# SonicBOOM Speculative Attacks

This repository holds all the work-in-progress code used to check if SonicBOOM is susceptible to Spectre attacks. This is work is based on the [boom-attacks](https://github.com/riscv-boom/boom-attacks).

# Further Details

## BOOM Configuration

This is working with the version of SonicBOOM located at [this commit](https://github.com/riscv-boom/riscv-boom/commit/96409013ee7a1e0aebfb535d5ad40a8e9b53e97b).

## Implemented Attacks

The following attacks are upgraded within the repo.

* Spectre-v1 or Bounds Check Bypass [1]
    * condBranchMispred.c
* Spectre-v2 or Branch Target Injection [1]
    * indirBranchMispred.c
* Return Stack Buffer Attack [2]
    * returnStackBuffer.c

# Building the tests

To build you need to run `make`

# Running the Tests

This builds "baremetal" binaries that can directly run on the BOOM configuration that was specified above.

# References

[1] P. Kocher, D. Genkin, D. Gruss, W. Haas, M. Hamburg, M. Lipp, S. Mangard, T. Prescher, M. Schwarz, and Y. Yarom, “Spectre attacks: Exploiting speculative execution,” ArXiv e-prints, Jan. 2018

[2] E. M. Koruyeh, K. N. Khasawneh, C. Song, N. Abu-Ghazaleh, “Spectre Returns! Speculation Attacks using the Return Stack Buffer,” 12th USENIX Workshop on Offensive Technologies, 2018
