jlab submit.sh
#!/bin/bash

#SBATCH --job-name=clas12Lambdastuff
#SBATCH --output=/farm_out/%u/%x-%j-%N.out
#SBATCH --error=/farm_out/%u/%x-%j-%N.err
#SBATCH --partition=gpu
#SBATCH --account=clas12
#SBATCH --mem-per-cpu=4000
#SBATCH --gres=disk:1000
#SBATCH --time=24:00:00
#SBATCH --mail-user=keegan.mencke@duke.edu
#SBATCH --gres=gpu:1

/work/clas12/users/mencke/job.sh

emacs


jlab job.sh
#!/bin/bash                                                  

export INFILE='/path/test.hipo'
export OUTDIR='/volatile/clas12/users/mencke/dir_name_2'
export name=`echo $INFILE | xargs -n 1 basename`
mkdir -p $OUTDIR
#cd ~/clas12work/mc_jobs_rga_ppim_2_23_24
cd /work/clas12/users/mencke/dir_name_2
#$C12ANALYSIS/bin/run.sh $INFILE -ch 2212,-211 -be 10.6 -tpid 2212 -rn -en -ang -vtx -lk -ik -ma -f -out $OUTDIR/skim_${name}.root
source /work/clas12/users/mencke/venvv/bin/activate.csh
#which python3

python3 testt_one.py 
echo DONE



Duke
sbatch –p (vossenlab-gpu) --account=(vossenlab)
par

submit duke
#!/bin/bash 

#SBATCH --job-name=vertex_nn
#SBATCH --output=/hpc/group/vossenlab/%u/farm_out/%x-%j-%N.out                                                                                                                                       
#SBATCH --error=/hpc/group/vossenlab/%u/farm_out/%x-%j-%N.err   
#SBATCH --partition=vossenlab-gpu
#SBATCH --account=vossenlab
#SBATCH --mem=4G
#SBATCH --time=24:00:00
#SBATCH --mail-user=keegan.mencke@duke.edu
#SBATCH --gres=gpu:1

/hpc/group/vossenlab/kam264/job.sh

                                                                                                                                                                                      




job.sh
#!/bin/bash
export INFILE='/path/test.hipo'
export OUTDIR='/volatile/group/vossenlab/dir_name_2'
export name=`echo $INFILE | xargs -n 1 basename`
mkdir -p $OUTDIR
cd /hpc/group/vossenlab/kam264/dir_name_2
#source /work/clas12/users/mencke/venvv/bin/activate.csh

python3 test_one.py 











SBATCH --output=/hpc/group/vossenlab/%u/farm_out/%x-%j-%N.out                                                                                                                                                    
#SBATCH --error=/hpc/group/vossenlab/%u/farm_out/%x-%j-%N.err                                                                                                                                                     
#SBATCH -p vossenlab-gpu                                                                                                                                                                                          
#SBATCH -c 8                                                                                                                                                                                                      
#SBATCH --gres=gpu:1                                                                                                                                                                                              
#SBATCH --mem-per-cpu=8G    







am264@dcc-login-01  ~ $ cd /hpc/group/vossenlab/mkam264
-bash: cd: /hpc/group/vossenlab/mkam264: No such file or directory
kam264@dcc-login-01  ~ $ cd /hpc/group/vossenlab/kam264
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ ls
dir_name_2  ENTER  farm_out  job.sh  Miniconda3-latest-Linux-x86_64.sh  pyg_test_rec_traj_dataset_111  submit_EXAMPLE.sh  submit_EXAMPLE.sh~  submit.sh  test_one.py
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ emacs job.sh
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ emacs submit.sh
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ ls farm_out
vertex_nn-11832629-dcc-vossenlab-gpu-04.err  vertex_nn-11832629-dcc-vossenlab-gpu-04.out
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ cat farm_out/vertex_nn-11832629-dcc-vossenlab-gpu-04.err
/var/spool/slurmd/job11832629/slurm_script: line 13: /hpc/group/vossenlab/kam264/job.sh: Permission denied
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ chmod +x job.sh
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ chmod submit.sh
chmod: missing operand after ‘submit.sh’
Try 'chmod --help' for more information.
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ chmod +x submit.sh
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ cd ..
kam264@dcc-login-01  /hpc/group/vossenlab $ cd kam264
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ ./submit.sh
mkdir: cannot create directory ‘/volatile’: Permission denied
testing_1
Traceback (most recent call last):
  File "/hpc/group/vossenlab/kam264/dir_name_2/test_one.py", line 7, in <module>
    from tqdm import tqdm
ModuleNotFoundError: No module named 'tqdm'
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ emacs job.sh
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ ./submit.sh
testing_1
Traceback (most recent call last):
  File "/hpc/group/vossenlab/kam264/dir_name_2/test_one.py", line 9, in <module>
    import torch
ModuleNotFoundError: No module named 'torch'
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ fname 
dir_name_2/                        job.sh                             pyg_test_rec_traj_dataset_111/     submit.sh                          
ENTER/                             job.sh~                            submit_EXAMPLE.sh                  submit.sh~                         
farm_out/                          Miniconda3-latest-Linux-x86_64.sh  submit_EXAMPLE.sh~                 test_one.py                        
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ fname 
dir_name_2/                        job.sh                             pyg_test_rec_traj_dataset_111/     submit.sh                          
ENTER/                             job.sh~                            submit_EXAMPLE.sh                  submit.sh~                         
farm_out/                          Miniconda3-latest-Linux-x86_64.sh  submit_EXAMPLE.sh~                 test_one.py                        
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ fin
fincore                find                   find-debuginfo         find-debuginfo.sh      findfs                 findmnt                find-repos-of-install  
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ find -help
Usage: find [-H] [-L] [-P] [-Olevel] [-D debugopts] [path...] [expression]

default path is the current directory; default expression is -print
expression may consist of: operators, options, tests, and actions:
operators (decreasing precedence; -and is implicit where no others are given):
      ( EXPR )   ! EXPR   -not EXPR   EXPR1 -a EXPR2   EXPR1 -and EXPR2
      EXPR1 -o EXPR2   EXPR1 -or EXPR2   EXPR1 , EXPR2
positional options (always true): -daystart -follow -regextype

normal options (always true, specified before other expressions):
      -depth --help -maxdepth LEVELS -mindepth LEVELS -mount -noleaf
      --version -xautofs -xdev -ignore_readdir_race -noignore_readdir_race
tests (N can be +N or -N or N): -amin N -anewer FILE -atime N -cmin N
      -cnewer FILE -ctime N -empty -false -fstype TYPE -gid N -group NAME
      -ilname PATTERN -iname PATTERN -inum N -iwholename PATTERN -iregex PATTERN
      -links N -lname PATTERN -mmin N -mtime N -name PATTERN -newer FILE
      -nouser -nogroup -path PATTERN -perm [-/]MODE -regex PATTERN
      -readable -writable -executable
      -wholename PATTERN -size N[bcwkMG] -true -type [bcdpflsD] -uid N
      -used N -user NAME -xtype [bcdpfls]      -context CONTEXT

actions: -delete -print0 -printf FORMAT -fprintf FILE FORMAT -print 
      -fprint0 FILE -fprint FILE -ls -fls FILE -prune -quit
      -exec COMMAND ; -exec COMMAND {} + -ok COMMAND ;
      -execdir COMMAND ; -execdir COMMAND {} + -okdir COMMAND ;

Valid arguments for -D:
exec, opt, rates, search, stat, time, tree, all, help
Use '-D help' for a description of the options, or see find(1)

Please see also the documentation at http://www.gnu.org/software/findutils/.
You can report (and track progress on fixing) bugs in the "find"
program via the GNU findutils bug-reporting page at
https://savannah.gnu.org/bugs/?group=findutils or, if
you have no web access, by sending email to <bug-findutils@gnu.org>.
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ find test
find: ‘test’: No such file or directory
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ ls *
job.sh  job.sh~  Miniconda3-latest-Linux-x86_64.sh  submit_EXAMPLE.sh  submit_EXAMPLE.sh~  submit.sh  submit.sh~  test_one.py

dir_name_2:
test_one.py

ENTER:
bin  cmake  compiler_compat  _conda  condabin  conda-meta  envs  etc  include  lib  LICENSE.txt  man  pkgs  sbin  share  shell  ssl  x86_64-conda_cos7-linux-gnu  x86_64-conda-linux-gnu

farm_out:
vertex_nn-11832629-dcc-vossenlab-gpu-04.err  vertex_nn-11832629-dcc-vossenlab-gpu-04.out

pyg_test_rec_traj_dataset_111:
processed
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ ls ~/*
'/hpc/home/kam264/makeing file.ipynb'   /hpc/home/kam264/pytorch_testt.ipynb              /hpc/home/kam264/test.ipynb   /hpc/home/kam264/Untitled1.ipynb   /hpc/home/kam264/Untitled3.ipynb
'/hpc/home/kam264/NN test 1.ipynb'     '/hpc/home/kam264/submit.sh and job for jlab.md'   /hpc/home/kam264/test.sh      /hpc/home/kam264/Untitled2.ipynb   /hpc/home/kam264/Untitled.ipynb

/hpc/home/kam264/data:
FashionMNIST

/hpc/home/kam264/drop:
drop

/hpc/home/kam264/ondemand:
data
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ emacs submit.sh
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ emacs job.sh
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ sbatch submit.sh
Submitted batch job 11866925
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ cat farm_out/vertex_nn-11866925-dcc-vossenlab-gpu-04.err
cat: farm_out/vertex_nn-11866925-dcc-vossenlab-gpu-04.err: No such file or directory
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ squeue -u menkce
squeue: error: Invalid user: menkce

             JOBID PARTITION     NAME     USER ST       TIME  NODES NODELIST(REASON)
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ squeue -u kam264
             JOBID PARTITION     NAME     USER ST       TIME  NODES NODELIST(REASON)
          11865682 vossenlab sys/dash   kam264  R    1:05:35      1 dcc-vossenlab-gpu-01
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ ls /farm_out
ls: cannot access '/farm_out': No such file or directory
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ ls farm_out
vertex_nn-11832629-dcc-vossenlab-gpu-04.err  vertex_nn-11832629-dcc-vossenlab-gpu-04.out  vertex_nn-11866925-dcc-vossenlab-gpu-02.err  vertex_nn-11866925-dcc-vossenlab-gpu-02.out
kam264@dcc-login-01  /hpc/group/vossenlab/kam264 $ cd farm_out
kam264@dcc-login-01  /hpc/group/vossenlab/kam264/farm_out $ emacs vertex_nn-11866925-dcc-vossenlab-gpu-02.err
kam264@dcc-login-01  /hpc/group/vossenlab/kam264/farm_out $ ^C
kam264@dcc-login-01  /hpc/group/vossenlab/kam264/farm_out $ ^C


how to copy from jlab to duke. 
#in jlab, files should be /work/clas12/users/mencke/<file name>   
need to move them to drop
do this by mv /work/clas12/users/mencke/<file name> ~/drop 
    
then to move to duke type 
rsync -r -v mencke@scilogin.jlab.org:~/drop/<file name> ~/drop/
once it is in duke, will need to move it out of drop
mv ~/drop/<file name> /hpc/group/vossenlab/kam264  




     
    
    
I think his sibatch submit example, submit_EXAMPLE.sh~
    
    
    
    
    
    
    
    