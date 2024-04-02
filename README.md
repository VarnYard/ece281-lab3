# Lab 3: Thunderbird Turn Signal

VHDL for ECE 281 [Lab 3](https://usafa-ece.github.io/ece281-book/lab/lab3.html)

Targeted toward Digilent Basys3. Make sure to install the [board files](https://github.com/Xilinx/XilinxBoardStore/tree/2018.2/boards/Digilent/basys3).

Tested on Windows 11.

---

## Build the project

You can simply open `thunderbird.xpr` and Vivado will do the rest!

## GitHub Actions Testbench

The workflow uses the [setup-ghdl-ci](https://github.com/ghdl/setup-ghdl-ci) GitHub action
to run a *nightly* build of [GHDL](https://ghdl.github.io/ghdl/).

The workflow uses GHDL to analyze, elaborate, and run the entity specified in the `.github/workflows/testbench.yml`.

```yaml
env:
  TESTBENCH_ENTITY: myfile
```

If successful then GHDL will quietly exit with a `0` code.
If any of the `assert` statements fail **with** `severity error` then GHDL will cease the simulation and exit with non-zero code; this will also cause the workflow to fail.




![image](https://github.com/VarnYard/ece281-lab3/assets/142039672/5ad6c231-9f45-40f6-a924-9f39a4a3eaab)





## Documentation Statement 

  ##C3C Shearer helped me with fixing my PreLab to get a better start on the Lab code and logic equations. 
  ##C3C Janssen helped me with my logic statements and verified that they were correct. I had flipped my f_Q(0) and f_Q(2) which was the main issue. He also helped me with some other minor mistakes. 
  ##I used ChatOpenAI to help me determine how I was going to write my test bench. I used the code provided very closely, only slightly editing it to make more sense for my specific needs. 
    ##It was only used on the test bench and not anywhere else in my code. 
