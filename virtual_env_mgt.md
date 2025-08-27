# Conda venv
## Create a conda Environment 
```bash
conda create --name myenv
or 
conda create -n venv python=3.10 -y
conda activate venv
conda deactivate
```

## Create a folder specific conda Environment 
```bash
mkdir myproject
cd myproject
conda create -p ./medibot python==3.9 -y
conda activate ./medibot
or 
# Activate by Full Path
conda activate "E:\Projects_Productionization\01-Chatbots-Projects\P011-medical-chatbot-local\medibot"
# Register Custom Envs in .condarc (Best Way)

conda deactivate
```

## Step 1: Create a conda environment inside your project folder
```bash
cd /path/to/your/project
conda create --prefix ./env python=3.10
```
## Step 2: Activate the environment
```bash
conda activate ./env
conda deactivate
```
## Step 3: Installing packages in that environment
```bash
conda install numpy pandas
pip install opencv-python retina-face
```

```bash
conda --version
conda update conda
conda search numpy
conda update numpy
conda clean --all # Clean Cache to Free Up Space
# important packages installed in any of those envs, consider exporting them first:
conda env export --name ENV_NAME > ENV_NAME.yml 
conda env export > environment.yml 
# recreate
conda env create -f ENV_NAME.yml 
conda env create -f environment.yml 

conda list # List Installed Packages

conda env list
conda info --envs
```
# removing conda env
```bash
conda env remove --prefix "E:\Projects_Productionization\01-Chatbots-Projects\P011-medical-chatbot-local\medibot"

conda env remove --name medibot # emove the one in your global .conda folder
conda env remove --name mlproj # C:\Users\surface\.conda\envs\mlproj