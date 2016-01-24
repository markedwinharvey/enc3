`enc3.py` is the third installment in our quest to generate a convenient substitution/permutation network encryptor. This version can be invoked directly from the command line by utilizing a bash function in conjunction with enc3.py, saved in or around the home directory. 

One or more files can be encrypted at the same time, or a single folder and its contents. This process can be carried out using a command such as:

enc3 -e a b c

which invokes enc3.py in encryption mode (-e) to serialize and encrypt files a, b, and c. 

The function is called with the enc3 command, followed by "-e" or "-d", and then the file(s) or folder. Error handling has been built in. 

The bash function is as follows:

enc3 () {
	python ~/enc3.py $@
	# or
	# python $HOME/enc3.py $@
}	

if enc3.py is located in the home directory. 
