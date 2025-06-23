# Deep-Kernel-Greedy

## Description
This is the code repository for the paper: Marian Klink, Tobias Ehring, Robin Herkert, Robin Lautenschlager, Dominik Göddeke and Bernard Haasdonk. "Solving Approximation Tasks with Greedy Deep Kernel Methods". (2025).
It implements the deep Vectorial Kernel Orthogonal Greedy Algorithm (deep VKOGA) that can be used to approximate a variety of functions based on underlying datasets. In particular, this repository includes the approximation of 
simple functions, breakthrough curves from chemcial species flowing through 3D porous media and parametrized ODEs. 
Further, it implements NNs and GNNs for the purpose of comparison.

## Dependencies
See the requirements.txt file for details. Main Python libraries are numpy, matplotlib, scipy, scikit-learn, pytorch, openpyxl, pandas, tqdm

## Notes
This project is structured in 5 major folders:
1. Utilities: Contains utilities for cross-validation, sampling, documentation and plotting.
2. Solvers: Contains the major solver implementations, such as deep VKOGA, DNN and GNN
3. Model_Problems: Contains the modelproblems/datasets corresponding to the function approximation and PODE solution approximation task.
4. PODE_Approximation: Contains the execution, evaluation and results corresponding to the PODE approximation problem.
5. Function_Approximation: Contains the execution, evaluation and results corresponding to the simple function approximation problem.
6. BTCurve_Approximation: Contains the execution, evaluation and results corresponding to the breakthrough curve approximation problem.

Especially the Function_Approximation folder/files can be used for any straight-forward approximation task, which is entirely provided by data and labels.

## Execution workflow
To execute the code, one can proceed as follows:
1. The ..._execute.py files can be executed via the commandline (see the file for details/examples) to fit any model on a given dataset or to perform an entire cross-validation.
2. The ..._evaluate.py files can be executed via the commandline (see the file for details/examples) to evaluate any fitted model, which is automatically stored as .npy file after calling ..._execute.py,
   on given test datasets and to store a dictionary of results (result_dict.npy) containing error or runtime measures.
3. In the result.ipynb notebooks, one can visualize the result dictionaries and create the plots.

## Reproducing/Analyzing Paper Plots
To reproduce/analyze the paper plots, the ...Result_Files folder contains .npy files corresponding to the fitted models. These .npy files can simply be loaded in the ..._valuate.py files to recreate the evaluation data. 
Further, these folders also contain excel sheets listing cross-validation scores of all validated architectures and .txt files specifying the final models after cross-validation. The plots are created in the corresponding 
.ipynb notebooks.

## Citation
If you use this code or want to cite this repository, please cite the paper.
