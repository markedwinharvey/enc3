`enc3.py` is the third installment in our quest to generate a convenient substitution/permutation network encryptor for python2.7. This version can be invoked directly from the command line by utilizing a bash function in conjunction with enc3.py, saved in or around the home directory. 

One or more files can be encrypted at the same time, or a single folder and its contents. For multi-file encryption, the files are first serialized. This process can be carried out using a command such as:

enc3 -e a b c

which invokes enc3.py in encryption mode (-e) to serialize and encrypt files a, b, and c (located in the working directory).  

Decryption runs the substitution/permutation steps in reverse and is called with the parameter "-d". When the script is run directly (as `enc3`), the next parameter must be the mode (or nothing), followed by files (if any). Error handling is built in.

The .bashrc function is as follows:

enc3 () {
	python ~/enc3.py $@
}	

*or*

enc3 () {
	python $HOME/enc3.py $@
}

if enc3.py is located in the home directory. 

enc3.py can also be invoked using `python enc3.py` from the directory in which the script is located. 
