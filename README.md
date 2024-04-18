# Lab 4: Advanced Elevator Controller

VHDL for ECE 281 [Lab 4](https://usafa-ece.github.io/ece281-book/lab/lab4.html)

Targeted toward Digilent Basys3. Make sure to install the [board files](https://github.com/Xilinx/XilinxBoardStore/tree/2018.2/boards/Digilent/basys3).

Tested on Windows 11.

---

## Build the project

You can simply open the `.xpr` and Vivado will do the rest!

## GitHub Actions Testbench

The workflow uses the [setup-ghdl-ci](https://github.com/ghdl/setup-ghdl-ci) GitHub action
to run a *nightly* build of [GHDL](https://ghdl.github.io/ghdl/).

The workflow uses GHDL to analyze, elaborate, and run the entity specified in the `.github/workflows/testbench.yml`.

```yaml
env:
  TESTBENCH_ENTITY: myfile
```

If successful then GHDL will quietly exit with a `0` code.
If any of the `assert` statements fail **with** `severity failure` then GHDL will cease the simulation and exit with non-zero code; this will also cause the workflow to fail.
Assert statements of other severity levels, such as "error" w

## DOC STATEMENT: C3C Janssen and I worked together as lab partners. C3C Jacob Lawrence helped me to write lines 234-243 in the top_basys3.vhd file

## DEMO: https://usafa0-my.sharepoint.com/:v:/g/personal/c26andres_samson_afacademy_af_edu/ERlXcmUw0_5BgQ2w_iJCXHgBqcSJbV89-MUEHHCX5Og2Lw?e=605TXS

## Lab report: https://usafa0-my.sharepoint.com/:b:/g/personal/c26andres_samson_afacademy_af_edu/EV2BFh12HRpAh_3xeqxwwwwBgm-QvZm-wqFvsaBiOeV1KQ?e=6adCnP

