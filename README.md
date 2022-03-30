# ComputerVision-Learning
Computer Vision Lectures & Learning from many University Courses 
1. CS231n - Stanford (EECS498 - Michigan)
2. AI604 - KAIST 
<br></br>

## Good to use AWS SageMaker when running code!
1. Sign-in(login) to your AWS console
2. Go to "Amazon SageMaker"
3. Go to "Dashboard" and create your SageMaker domain
4. Go to "Notebook" and create your Notebook instance (p3.2xlarge is good!)
5. When the notebook instance is created, you can start JupyterLab!

### Make custom environment in your JupyterLab
1. Launch your JupyterLab and open terminal
2. Here is needed command lines!
   ```bash
   sh-4.2$ source activate python3
   (python3) sh-4.2$ pip install theano
   (python3) sh-4.2$ source deactivate
   (JupyterSystemEnv) sh-4.2$
   ```
3. You can upload your data or .ipynb, .py files.
   - It's located in "SageMaker" directory
   ```bash
   sh-4.2$ cd SageMaker
   ```
4. You can create your own virtual conda environment and ipykernel
   - If you have environment yml file,
   ```bash
   (JupyterSystemEnv) sh-4.2$ conda create env -f [filename].yml
   ```
   - Or create your own!
   ```bash
   (JupyterSystemEnv) sh-4.2$ conda create -n [env_name] python=3.x
   ```
   - Then you can create kernel spec
   ```bash
   (JupyterSystemEnv) sh-4.2$ conda activate [virtualEnv]
   (virtualEnv) sh-4.2$ python -m ipykernel install --user --name [virtualEnv] --display-name "[displayKenrelName]"
   ```
   - You can check at .ipynb file "Kernel"!
