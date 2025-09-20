# essence-riscv
RISC-V Tapeout

<details>
  <summary>Week - 0: Installation of Tools and SoC Workflow Overview</summary>

  ### System Requirements
  - Minimum 6GB RAM
  - 50GB HDD
  - Ubuntu 20.04+ (recommended)
  - 4 vCPU

  ### Oracle Virtual Machine
  - Download: [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

  ### Tool Check

  <details>
    <summary>Yosys Installation</summary>
    ```
    sudo apt-get update
    git clone https://github.com/YosysHQ/yosys.git
    cd yosys
    sudo apt install make   # If make is not installed
    sudo apt-get install build-essential clang bison flex \
      libreadline-dev gawk tcl-dev libffi-dev git \
      graphviz xdot pkg-config python3 libboost-system-dev \
      libboost-python-dev libboost-filesystem-dev zlib1g-dev
    make config-gcc
    make
    sudo make install
    ```
  </details>

  <details>
    <summary>Icarus Verilog Installation</summary>
    ```
    sudo apt-get update
    sudo apt-get install iverilog
    ```
  </details>

  <details>
    <summary>GTKWave Installation</summary>
    ```
    sudo apt-get update
    sudo apt install gtkwave
    ```
  </details>

  ### SoC Workflow Summary

  - Chip modelling begins with specs in C and a testbench written in C.
  - A soft copy of the hardware is created using RTL (Verilog) for SoC design flow.
  - The SoC consists of processor cores and peripherals/IPs subdivided for modular design.
  - Components undergo gate-level netlist synthesis, macro synthesis, and analog IP functional modeling.
  - SoC integration assembles all blocks, including GPIOs, floorplanning, placement, clock tree synthesis, and routing for physical design.
  - Physical design leads to GDSII layout, followed by design rule checks (DRC/LVS).
  - Final SoC verification ensures all design stages are functionally equivalent (O1 = O2 = O3 = O4).
  - Resulting SoCs run at target frequencies (typically 100–130 MHz) and are applied in products like smartwatches, Arduino boards, TV panels, and AC applications.
  - Testbenches remain in C language throughout verification for consistency and speed.

</details>
