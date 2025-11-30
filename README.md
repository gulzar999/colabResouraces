🧪 HybridEGFR Generative Cheminformatics Pipeline

A complete deep learning workflow for novel molecule generation and descriptor calculation targeting EGFR.

1. Description

This project encapsulates a full Generative Chemistry pipeline designed to discover and evaluate novel lead compounds, primarily focused on the EGFR (Epidermal Growth Factor Receptor) target. The workflow involves several key stages:

Data Acquisition: Fetching bioactivity data from the ChEMBL database.

Model Training: Training a deep learning model  on the collected data.

Novel Generation: Using the trained model to generate novel, synthetically viable chemical structures (SMILES).

Descriptor Calculation: Processing the generated structures to calculate essential physicochemical and structural descriptors using RDKit, making them ready for further QSAR/QSPR analysis and filtering.

The project solves the problem of in silico lead discovery, accelerating the initial screening phase of drug R&D. The target audience includes computational chemists, deep learning engineers, and medicinal chemists looking to apply AI to drug discovery.

2. Features

Data Curation: Automated retrieval and processing of relevant bioactivity data directly from the ChEMBL database.

Deep Learning Integration: Foundation for training or utilizing a deep learning generative model (like a VAE or RNN) for de novo molecule design.

Novel Molecule Generation: Produces novel chemical entities with high potential for desired biological activity.

RDKit Descriptor Calculation: Processes generated SMILES to calculate key properties (LogP, TPSA, Molecular Weight, etc.).

Output Ready: Generates a final CSV dataset containing generated molecules and their calculated descriptors, suitable for downstream analysis or virtual screening.

3. Demo (Optional)

A walkthrough of the descriptor calculation workflow is fully contained within the hybridegfr.ipynb file itself. See the final CSV output structure here: (Link to a hosted sample CSV or a screenshot of the DataFrame)

4. Installation and Setup

This project requires a Python environment and standard scientific computing libraries, plus deep learning frameworks for the model training/generation components.

Prerequisites

Python (3.8+): Required for the notebook environment.

Jupyter Notebook/Lab: Recommended environment for running the .ipynb file.

Step-by-Step Instructions

Clone the Repository:

git clone [https://github.com/YourUsername/HybridEGFR-Descriptors.git](https://github.com/YourUsername/HybridEGFR-Descriptors.git)
cd HybridEGFR-Descriptors


Install Dependencies:
This project uses pip to manage required libraries. Note that deep learning libraries are assumed based on your description.

# Create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`

# Install the necessary packages (including assumed deep learning frameworks)
pip install pandas chembl_webresource_client rdkit tensorflow # or pytorch if preferred


Start the Jupyter Environment:

jupyter notebook
# or
jupyter lab


Run the Workflow: Open the hybridegfr.ipynb file in your browser. This notebook specifically handles descriptor calculation for the molecules generated in the previous step.

5. Usage

The hybridegfr.ipynb notebook handles the descriptor calculation stage, taking the output from the generative model as input.

Prerequisite Step (External to this Notebook): Run the deep learning model to generate a set of novel SMILES strings and save them to a CSV file (e.g., generated_smiles.csv).

Prepare Input Data: Ensure this generated CSV file has a column containing the valid SMILES strings (e.g., named 'generated_smiles').

Update Execution Block: Modify the EXECUTION BLOCK at the end of the notebook to point to your specific file and column names:

calculate_descriptors(
    smiles_file_path="generated_smiles.csv",
    smiles_column='generated_smiles'
)


Execute: Run the final code cell. The script will generate a new file, descriptors_output.csv, containing the generated molecules plus the calculated descriptors.

6. Technology Stack

Primary Language: Python

Data Retrieval: ChEMBL Web Resource Client

Data Manipulation: Pandas

Cheminformatics: RDKit (Crucial for molecular processing and descriptor generation)

Deep Learning (Assumed): TensorFlow / PyTorch (For molecule generation model)

Environment: Jupyter Notebook

7. License

This project is licensed under the MIT License. See the LICENSE file for details.

8. Contributing

Contributions, issues, and feature requests are highly welcome! If you have suggestions for new generative models, different data curation strategies, or improvements to the descriptor calculation workflow, please feel free to fork the repository and submit a Pull Request.

 ## for quries can here out to this email >>>> gulzarasma2@gmail.com
