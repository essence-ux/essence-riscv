# essence-riscv
RISC-V Tapeout 
<details>
  <summary>Week - 0: Installation of Tool</summary>

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

</details>
