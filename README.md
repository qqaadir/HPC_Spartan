# HPC Spartan Commands
Add linux commands and relevant resources to run jobs (for TensorFlow, MATLAB) on GPU partition of HPC Spartan.


### Running interactive jobs

 `sinteractive --partition=shortgpgpu --gres=gpu:p100:1 -q gpgpumse --mem=16g --time=01:00:00`
 
 shortgpgpu partition can only allow 1 hr of interactive job time. Switch to gpgpu for longer time
