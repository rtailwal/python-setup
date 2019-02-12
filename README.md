# Setup Virtual Enviroment for new python setup
Follow the below commands.

Create a new directory

1. mkdir Software

2. cd Software

3. Download the particular version of Python. In this case I am suing Python3.5.5

  wget  https://www.python.org/ftp/python/3.5.5/Python-3.5.5.tar.xz
  
4. Extract the tar file

   unxz Python-3.4.1.tar.xz
   
   tar xvf Python-3.4.1.tar
   
5. Go to the Python directory and install

    cd Python-3.5.5

    ./configure --prefix=/home/user/Software/Python-3.4.1/mybuild

    make

    make install
  
6. Create virtual environment and activate it. You should see the python3.5.5 version on running python command in the virtualenv

  virtualenv --python=/home/<user>/Software/Python3.5.5/mybuild/bin/python3.5 virtualenv3
  
  cd virtualenv3
  
  source bin/activate
  
  python
 
 

  Notes: Its good to have the basic dev tools in the system. If you get errors related to compiler or zip etc make sure to run below commands to install those before make install in step 5.
  
    apt-get install build-essential
  
    apt-get install libssl-dev
    
    apt-get install make build-essential libssl-dev zlib1g-dev libbz2-dev libsqlite3-dev
    
    
    
Install pip if not installed

  apt-get install python3-pip
