# HPC Spartan Commands
Add linux commands and relevant resources to run jobs (for TensorFlow, MATLAB) on GPU partition of HPC Spartan.


### Running interactive jobs

 `sinteractive --partition=shortgpgpu --gres=gpu:p100:1 -q gpgpumse --mem=16g --time=01:00:00`
 
 shortgpgpu partition can only allow 1 hr of interactive job time. Switch to gpgpu for longer time. Use the following command
 
  `sinteractive --partition=gpgpu --gres=gpu:p100:1 -q gpgpumse --mem=16g --time=05:00:00`

The above command allows to use gpu partition for 5 hrs. After this command, [MObaXterm](https://mobaxterm.mobatek.net/) can be used to load various GUI modules, for example, you can use the following command to run MATLAB:

`module load matlab`

`matlab`
 
A comprehensive list and explanation of HPC commands can be found [here](https://github.com/UoM-ResPlat-DevOps/SpartanIntro). 

 `du -hs .[^.]*` 
 
 The above command can be used to check for diskspace.
