echo "Install cuda10 & cunn "

echo "PRESS [ENTER] TO CONTINUE THE INSTALLATION"
echo "IF YOU WANT TO CANCEL, PRESS [CTRL] + [C]"
read


echo "[Install cuda10.0 & cudnn7.6.3]"

sudo dpkg -i cuda-repo-ubuntu1604-10-0-local-10.0.130-410.48_1.0-1_amd64.deb
sudo apt-key add /var/cuda-repo-10-0-local-10.0.130-410.48/7fa2af80.pub
sudo apt-get update
sudo apt-get -y install cuda

export PATH=/usr/local/cuda/bin:$PATH
export LD_LIBRARY_PATH=/usr/local/cuda/64:$LD_LIBRARY_PATH
source ~/.bashrc


echo "###################"
echo "###################"

nvcc -V

echo "###################"
echo "###################"


sudo dpkg -i libcudnn7_7.6.3.30-1+cuda10.0_amd64.deb
source ~/.bashrc


echo "[Setup env, use pip]"
sudo apt-get -y install python3-pip python3-dev python-virtualenv
sudo apt -y install cmake


source ~/.bashrc

echo "Install Finish!!!"

