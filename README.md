# NNcross

Model state-to-state cross section for atom-diatom collisions

**Requirements**

python3 and TensorFlow

**How to train**

Edit the utlty.py and training.py according to specify data set size and and learning rate and training type.
Then run the training.py code by mentioning number of training data, validation data, seed, number of training epochs and batch size.

`python3 training.py 8000 2000 11 2000 500`

**How to get the the optimized parameters**

Run the print_coeff.py with same number of training and validation data.

`python3 print_coeff.py 8000 2000 11 2000 500`

**How to predict the cross sections**

Compile the nn_sts_cs.f90 code with fortran compiler. The fortran code uses all the 'Coeff_' files generated by the print_coeff.py code and ro-vibrational state details for the diatoms.
