cd

pip3 install --upgrade pip
pip3 install jupyter

virtualenv --system-site-packages -p python3 ~/pytorch_g
source ~/pytorch_g/bin/activate
python -m ipykernel install --user --name torch --display-name "torch"

pip3 install torch torchvision


echo "pytorch version"
python -c "import torch; print(torch.__version__)"

sh -c "echo \"alias spg='source ~/pytorch_g/bin/activate'\" >> ~/.bashrc"

echo "Everytime you want to get into virtualenv of pytorch, just typing [ spg ]"

deactivate

cd

virtualenv --system-site-packages -p python3 ~/tfkeras_g
source ~/tfkeras_g/bin/activate
python -m ipykernel install --user --name tf --display-name "tf"

echo "[Download and install pytorch]"
pip3 install tensorflow-gpu
pip3 install keras

sh -c "echo \"alias stf='source ~/tfkeras_g/bin/activate'\" >> ~/.bashrc"

deactivate

echo "Install Finish!!!"
