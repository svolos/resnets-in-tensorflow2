1. Build tensorflow container with packages required for resnet

`sudo docker build -t tensorflow:resnet .`

2. Test tensorfolow container with toy example

`docker run -it --rm tensorflow:resnet python -c "import tensorflow as tf; print(tf.reduce_sum(tf.random.normal([1000, 1000])))"`

3. Switch to parent directory and run tensorflow container

`pushd ../`
`sudo docker run -it --rm -v $PWD:/tmp -w /tmp tensorflow:resnet python run_resnets.py`
