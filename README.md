# gaussian_riscv-vp


one can download the updates source code to their working directory
  git clone https://github.com/freud96/gaussian_riscv-vp.git
  
  copy the accelerator virtual platform
  $ cp -r gaussian_riscv_vp/riscv-vp/vp/src/platform/* $<working directory>/riscv-vp/vp/src/platform
  
  copy the software code
  $ cp -r gaussian_riscv_vp/riscv-vp/sw/* $<working directory>/riscv-vp/sw
  
  go to basic-acc/build under the riscv-vp directory and do the following:
  $ cmake ..
  $ make install
  
  build the gaussian blur software:
  go to basic-gaussian under sriscv-vp/sw and do 
  $ make
  $ make sim
