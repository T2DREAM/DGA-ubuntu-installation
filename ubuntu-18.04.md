# Installation & buildout on Ubuntu18.04

### **a) Install Python3.4.4 at /home/ubuntu/**  

  - `sudo wget https://www.python.org/ftp/python/3.4.4/Python-3.4.4.tgz` 
  - `tar -zxvf Python-3.4.4.tgz` 
  - `cd Python-3.4.4/` 
  - `./configure` 
  - `make install`
  
### **b) Create python3 venv**  

 - `sudo apt-get install libssl1.0` #installation of python modules requires openssl
 - `virtualenv --python=python3.4 --clear --always-copy --setuptools .t2dream-venv` #[install python3.4.4 on ubuntu18.04](https://askubuntu.com/questions/1108268/any-way-to-install-python-3-4-on-ubuntu-18-04)
 - `virtualenv .t2dream-venv --distribute` 
 - `source .t2dream-venv/bin/activate` 

### **c) Install npm & Node version mangement with nvm**

 - `sudo apt install npm` 
 - `curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.35.2/install.sh | bash`
 - ` export NVM_DIR="$HOME/.nvm"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"  # This loads nvm
 [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion"  # This loads nvm bash_completion
` 
- `nvm install 6` 
- `nvm use 6`
### **d) Install pip dependencies & run buildout**

[Install pip dependencies](https://github.com/T2DREAM/DGA-ubuntu-installation/pip-dependencies.txt) 
