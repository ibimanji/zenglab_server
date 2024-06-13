# login via ssh
You need to have an account in the server first. Contact Chen.

You can login the server via [ssh](https://en.wikipedia.org/wiki/Secure_Shell) by the following command line in your terminal:

```batchfile
ssh YourUserName@10.128.243.62
```

Alternatively, you can configure the ssh in your local file `~/.ssh/config` (you may need to make the `~/.ssh` folder first), and add the following lines:

```batchfile
Host labserver
    User YourUserName
    HostName 10.128.243.62
    ServerAliveInterval 5
```

Then you can login via the following command line:

```batchfile
ssh labserver
```
## Login remotely

The server is inside University's LAN, so you need to be in the unveristy's netweek physically or via the [University's VPN](https://its.pku.edu.cn/)

Once you are in the VPN, you can login via ssh as above section.

## Using MobaXterm 

For windows user, [mobaxterm](https://mobaxterm.mobatek.net/) is a useful for terminal managment 

please enter port 22 and your specific account name to login 

# File system(important!!!)
- `/home/YOU`: home directory ,which is SSD drive 2TB in total . please **DONOT** save sequencing file and your result under your home, its **huge** !! you may keep software (`conda environment`), intermediate data, or analyses here.
- Our main Storage disk (raid) is mounted on /media/zenglab now is 32TB in total ..(To be expanded) which contains:
	- `/media/zenglab/test/` you may keep test data files here
	- `/media/zenglab/data/` you may keep raw or large data files here
	- `/media/zenglab/result/` you may keep final output/analyze result here 
	- `/media/zenglab/script/` you may keep your software repo or scripts here
	- `/media/zenglab/miniconda3/` the public conda used for pipeline/snakemake repeat
you may create directory and use them as follows:
**`media/zenglab/TYPE/YOU`**

## future management plan
- we may transfer existing file from `/media/zenglab/data/` to user's own `media/zenglab/data/YOU` data and for previous rawdata in broad , we can create `zenghu` directory
- `/ssd/research`: for shared research projects, we will keep them here
