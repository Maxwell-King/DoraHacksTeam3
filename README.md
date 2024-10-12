# DoraHacksTeam3
Stages of the Challenge
Stage 1: Implementing a QRNG on IBM QPUs
Objective: Implement a simple quantum random number generator on an IBM quantum machine or simulator (if needed) and generate QRNG data.

Description: Use IBM Qiskit Simulators to create a circuit that measures qubits in equal superposition to generate quantum random numbers. This stage will help you understand the basics of quantum circuits and qubit measurement. Once this is relatively straightforward for you, try and generate QRNG data using actual IBM quantum computers (you will need to create a free account and use your API key) and analyze/visualize your results.

Resources:

Stage 2: Achieving High Accuracy with Classification Models
Objective: Use the provided model to classify QRNG data and aim for high accuracy.

Description: Train a classifier model to classify whether the data is quantum or classical random numbers, with a target accuracy of over 60% for input lengths of 100-1000 bit QRNG data. Attached in the resources section is skeleton code for training and testing a gradient boosting ML model with your dataset, as well as an example dataset you can use to classify quantum vs non-quantum data. Optional: Enhance the accuracy by building/optimizing your own models and exploring various machine learning hypertuning techniques. Optional: Attempt to classify with other variables, such as quantum simulator vs actual quantum computer data, or classify by actual IBM quantum computers. You will have to create your own training data sets. Our existing work in this area is also in the attached repo.

Stage 3: Characterizing Noise and Fidelity
Objective: Analyze the noise and fidelity of the quantum machine used for QRNG.

**Description:**Characterize the noise and fidelity of the IBM QPU to understand how these factors impact the quality of the generated random numbers. This stage involves data analysis and understanding the intricacies of quantum hardware performance. For an easier and more intermediate step, analyze the noise patterns of IBM/Qiskit quantum simulators. Good data visualizations are a plus. You can find official device-specific quantum noise related data such as decoherence, error rates, etc both on the official IBM quantum platform and through Qiskit.

Stage 4: Pre-processing and Post-processing for High Entropy
Objective: “Clean” the QRNG data you generated on IBM’s quantum computers to generate high entropy, classically distributed quantum random number data.

Description: Deploy pre-processing and post-processing techniques to enhance the entropy of the generated quantum random numbers. This stage focuses on data cleaning and improving the randomness quality of the QRNG data. Run your processed QRNG data through tests of randomness such as the NIST test suite for statistical randomness and present/analyze your results. Bonus: additionally, implement the QRNG data in a real-world application, such as an encryption protocol, to demonstrate its practical utility.

Stage 5: Building High-Accuracy Classification Models for QRNG Verification
Objective: Build on and/or include your work from stages 2, 3, and 4 in order to train high accuracy QRNG classification models.

Description: Implement your pre/post-processing methods and/or your noise/fidelity characterization solutions into a classification model (possibly one you developed in stage 2) to increase classification accuracy, especially for (A) classifying QRNG vs PRNG data and (B) classifying by specific quantum device (i.e. predicting what QPU a line of data is from). Currently, the highest performing models we have trained as part of the broader DoraHacks QRNG project only reach classification accuracy of >95% or >99% with binary training data string lengths of thousands of bits - for this stage, reliably high accuracy is more important than input size. You may wish to utilize advanced frequency signal detection methods such as fourier transforms or advanced deep learning procedures such as neural network architectures to find underlying patterns in the data. (HINT: quantum noise and fidelity will vary between quantum computers, and PRNG data will obviously not have any quantum noise reflected in the data, so any successful classification models will take advantage of these phenomena).
