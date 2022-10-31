# milestone-1
## installing nni and ngrok
### ! pip install nni # install nni
### ! wget https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-linux-amd64.zip # download ngrok and unzip it
### ! unzip ngrok-stable-linux-amd64.zip
### ! mkdir -p nni_repo
### ! git clone https://github.com/microsoft/nni.git nni_repo/nni # clone NNI's offical repo to get examples
##
## authorizing ngrok and opening
### ! sudo cp ngrok /usr/local/bin
### ! ngrok authtoken 2GsbfBgbr0cAwhH8SbzKyu5Lqtl_4ekshN1Mi5rHTK7JA5X3j
### ! nnictl create --config nni_repo/nni/examples/trials/mnist-pytorch/config.yml --port 5156 & 
### get_ipython().system_raw('./ngrok http 5156 &')
### ! curl -s http://localhost:4040/api/tunnels # don't change the port number 4040
