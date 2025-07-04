# AXIS TINY FIFO
### Simple single clock fifo
---

![image](docs/manual/img/AFRL.png)

---

  author: Jay Convertino   
  
  date: 2021.06.02  
  
  details: Simple axis single clock pipeline fifo.  
  
  license: MIT   
   
  Actions:  

  [![Lint Status](../../actions/workflows/lint.yml/badge.svg)](../../actions)  
  [![Manual Status](../../actions/workflows/manual.yml/badge.svg)](../../actions)  
  
---

### Version
#### Current
  - V1.0.0 - initial release

#### Previous
  - none

### DOCUMENTATION
  For detailed usage information, please navigate to one of the following sources. They are the same, just in a different format.

  - [axis_tiny_fifo.pdf](docs/manual/axis_tiny_fifo.pdf)
  - [github page](https://johnathan-convertino-afrl.github.io/axis_tiny_fifo/)

### PARAMETERS
* FIFO_DEPTH : DEFAULT = 4 : Set the depth of the single clock fifo (number of words the size of width).
* BUS_WIDTH  : DEFAULT = 8 : Set the data width of the fifo in bytes.

### COMPONENTS
#### SRC

* axis_tiny_fifo.v
  
#### TB

* tb_axis.v
* tb_cocotb.v
* tb_cocotb.py
  
### FUSESOC

* fusesoc_info.core created.
* Simulation uses icarus to run data through the core. Verification added.

#### Targets

* RUN WITH: (fusesoc run --target=sim VENDER:CORE:NAME:VERSION)
  - default (for IP integration builds)
  - lint
  - sim
  - sim_rand_data
  - sim_rand_ready_rand_data
  - sim_8bit_count_data
  - sim_rand_ready_8bit_count_data
  - sim_cocotb
