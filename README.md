# DLV (Deep Learning Verification)


NB: the software is currently under active development. Please feel free to contact the developer by email: xiaowei.huang@cs.ox.ac.uk. 

Together with the software, there are two documents in Documents/ directory, one is the theory paper and the other is an user manual. The user manual will be updated from time to time. Please refer to the documents for more details about the software. 

### Installation: 

To run the program, one needs to install the following packages:
           
           Python 2.7 
           
           conda install opencv numpy=1.13 scikit-image cvxopt  (need to install Anaconda first, see https://docs.anaconda.com/anaconda/install/)
           
           pip install stopit
           
           pip install keras==1.2.2 (Note: the software currently does not work well with Keras 2.x because of image dimension ordering problems, please use a previous 1.x version)
           
           pip install pySMT z3
           
           Note: there is some comparability problem on OpenCV. Please use version 2.4.*. 
           
           The z3 pacakge needs to be properly installed. You can follow the instruction: https://github.com/Z3Prover/z3, or run the following commands (tested on Mac OS): 
           
           git clone https://github.com/Z3Prover/z3.git
           cd z3
           python scripts/mk_make.py --python
           cd build
           make
           sudo make install
           
### Check the backend of Keras: 

The backend of Keras needs to be changed by editing the ~/.keras/keras.json file : 

    "backend": "theano",
    "image_dim_ordering": "th"
    
### Download dataset and network paramters. 

    If you want to train a network for GTSRB, Please download the dataset file X.h5 file from https://www.dropbox.com/s/2brjdjghhnmw6i7/X.h5?dl=0 to networks/ directory. For details on download networks and datasets for imageNet, please refer to the document. 

### Usage: 

Use the following command to call the program: 

           python DLV.py

Please use the file ''configuration.py'' to set the parameters for the system to run. 


Xiaowei Huang
