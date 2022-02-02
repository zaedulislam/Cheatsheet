<details>
  <summary>What is Conda?</summary>
  - Package, dependency and environment management for any language---Python, R, Ruby, Lua, Scala, Java, JavaScript, C/ C++, FORTRAN.
</details>


### Creating an environment with commands
By default, environments are installed into the `envs` directory in your conda directory.

- Use the terminal or an Anaconda Prompt for the following steps:
  1. To create an environment: `conda create --name myenv`
  2. When conda asks you to proceed, type `y`: `proceed ([y]/n)?`. This creates the `myenv` environment in `/envs/`. No packages will be installed in this environment.
  3. To create an environment with a specific version of Python: `conda create -n myenv python=3.8.2`
  
  

---

### Activating an environment
* To activate an environment: `conda activate myenv` [^1]
[^1]: Replace `myenv` with the environment name or directory path.

---

### Removing an environment
- To remove an environment, in your terminal window or an Anaconda Prompt, run: `conda remove --name myenv --all`
- You may instead use `conda env remove --name myenv`.

---

### Viewing a list of your environments
* To see a list of all of your environments, in your terminal window or an Anaconda Prompt, run:
`conda info --envs` OR `conda env list`

### Version Check

   Windows                      | Linux                         | Google Colaboratory 
-------------                   | -------------                 | ------------
Pending                         | `conda -V` or `conda --version`   | Pending

---

### Reference
1. https://docs.conda.io/projects/conda/en/latest/index.html
2. https://pypi.org/project/condacolab/
