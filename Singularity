Bootstrap: docker
From: ubuntu:16.04

%environment

  
%post
    echo "Update apt-get"
    apt-get -y update

    echo "Install python3"
    apt-get -y install python3-matplotlib python3-pip  
   
    ln -s /usr/bin/python3 /usr/bin/python
    
    echo "Install python packages"
    python3 -m pip install --upgrade pip numpy
    python3 -m pip install pandas spython scipy scikit-learn seaborn
%runscript
     exec /usr/bin/python3 $1 $2   
