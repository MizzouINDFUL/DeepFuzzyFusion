################################################################################
################################################################################
################################################################################
# Date:             AUG-16-2019
# Institution:      University of Missouri (Columbia, MO)
# Authors:          Blake Ruprecht, Muhammad Islam, and Derek Anderson
#
# DESCRIPTION ------------------------------------------------------------------
#    This is PyTorch code for an Adaptive Neural Fuzzy Inference System (ANFIS)
#
# Notes:
# 1. The below FuzzyNeuron class is a single fuzzy inference system (FIS)
#    What does that mean?
#    - Its a single first-order Takagi Sugeno Kang (TSK) inference system
#    What does that mean?
#    - Each neuron consists of R different IF-THEN rules and the aggregation of
#      their output.
# Coming soon...
#    - We will post cost updates that allow you to do things like
#    - Learn the number of rules R (via an algorithm like DBSCAN or
#      k-means/fcm/pcm with cluster validity)
#
# FOR MORE DETAILS, SEE: -------------------------------------------------------
#
#   Jang, "ANFIS: adaptive-network-based fuzzy inference system," IEEE
#       Transactions on Systems, Man and Cybernetics, 23 (3), 1993
#
# GNU GENERAL PUBLIC LICENSE ---------------------------------------------------
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <https://www.gnu.org/licenses/>.
#
##############################################################################
##############################################################################
##############################################################################
#
# INSTALLATION GUIDE
# 
# 1.) This is all Python 3.7 code, heavily utilizing PyTorch.
#     The following libraries must be installed to run:
#
#         torch
#         tqdm
#         matplotlib
#         scikit-learn
#         numpy
# 
#     We installed everything using conda. The following command (in a 
#     terminal) can be used to install each library (e.g. scikit-learn)
#
#         conda install -c conda-forge scikit-learn
#
# 2.) Once all of the relevant libraries are installed, make sure you have
#     the ???trapANFISPyTorchDeep.py??? and ???dataset_utils.py??? in the same directory,
#     since we will be using ???dataset_utils.py??? as a library within ???ANFIS??????
#
##############################################################################
##############################################################################
##############################################################################
#
# RUNNING THE PROGRAM
#
# Within the file ???ANFISPyTorchDeep.py??? we have an example to see how to use
# the main code. It is at the bottom of the file. The example will execute
# when the following command is run inside the terminal:
#     
#     python ANFISPyTorchDeep.py
#
# This will execute everything after the ???if __name__==???__main__???:??? statement
# in the code. The example is either a two-layer ANFIS (the if(0) statement),
# or a single ANFIS neuron.
#
# We recommend starting with the single neuron (which the code defaults to)
# Within this example, the number of rules to be learned and the number of 
# antecedents can be changed, along with the number of epochs. The code will
# plot the results using matplotlib, showing rule coverage.
#
# Finally, the initialization method can be changed within the instantiation
# of the FuzzyNeuron() class in the line ???net = FuzzyNeuron(R,A,2,x,l)???.
# The ???2??? can be changed to 0, 1, 2 and will change the initialization 
# method as explained in the __init__ section of the FuzzyNeuron class.
#
##############################################################################
##############################################################################
##############################################################################








