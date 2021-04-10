# HPC Spartan Commands
Add linux commands and relevant resources to run jobs (for TensorFlow, MATLAB) on GPU partition of HPC Spartan.


### Running interactive jobs

 `sinteractive --partition=shortgpgpu --gres=gpu:p100:1 -q gpgpumse --mem=16g --time=01:00:00`
 
 shortgpgpu partition can only allow 1 hr of interactive job time. Switch to gpgpu for longer time. Use the following command
 
  `sinteractive --partition=gpgpu --gres=gpu:p100:1 -q gpgpumse --mem=16g --time=12:00:00`

The above command allows to use gpu partition for 5 hrs. After this command, [MObaXterm](https://mobaxterm.mobatek.net/) can be used to load various GUI modules, for example, you can use the following command to run MATLAB:

`module load matlab`

`matlab`
 
A comprehensive list and explanation of HPC commands can be found [here](https://github.com/UoM-ResPlat-DevOps/SpartanIntro). 

 `du -hs .[^.]*` 
 
 The above command can be used to check for diskspace.

Sometime we create .slurm files on windows, this cause issues of compatibility with DOS command such as batch filename.slurm. The erros looks like this 

`sbatch: error: Batch script contains DOS line breaks (\r\n)\ sbatch: error: instead of expected UNIX line breaks (\n)  `

To handle this issues, we need to replace \r characters with \n. This can be done simply using notedpad++ on windows and replace all search occurances of the \r\n with \n. This will fix above errors. Note, make sure to use extended search in notepad++. More details can be found [here](https://wikis.ovgu.de/hpc/doku.php?id=guide:dos_unix_linebreaks).

