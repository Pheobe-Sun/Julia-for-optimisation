# Getting Started
You will use Jupyter Notebook, Julia (v1.6.2), and Xpress throughout the course.

## Install Anaconda and Jupyter Notebook
- If you already have Jupyter Notebook installed, go ahead and install Julia (jump right into the next step)
- If you don’t have Jupyter Notebook on your local machine, [install Anaconda](https://www.anaconda.com/products/individual-d)

## Install Julia
1. [Download Julia V1.6.2](https://julialang.org/downloads/) and install: follow the installation instructions
2. Open Julia Command-Line: in the windows search bar type in 'Julia' and click on 'Julia 1.6.2'
3. In Julia Command-Line, type the following commands one after another

    - Type in ``using Pkg`` and then press Enter
![type using Pkg in Julia Command-Line](https://github.com/Pheobe-Sun/Julia-for-optimisation/blob/main/static/Install_Julia_package1.PNG)

    - Then type in ``Pkg.add(“IJulia”)``, press Enter, and wait for the package to be added
![type using Pkg in Julia Command-Line](https://github.com/Pheobe-Sun/Julia-for-optimisation/blob/main/static/Install_Julia_package2.PNG)

4. Now let's create your first Julia notebook!
    - Run jupyter notebook. (If you are not familiar with Jupyter Notebook, follow the short instruction [here](https://pythonforundergradengineers.com/opening-a-jupyter-notebook-on-windows.html)) 
    - Click on the “New” button at the top right of your local jupyter notebook server, then choose “Julia 1.6.2”
    ![create new Julia notebook](https://github.com/Pheobe-Sun/Julia-for-optimisation/blob/main/static/Create_new_Julia_notebook.png)

    - Once a new jupyter notebook is set up, you should see Julia’s icon on the *top right* of the new notebook  
    ![check Julia's icon in newly-created notebook](https://github.com/Pheobe-Sun/Julia-for-optimisation/blob/main/static/Create_new_Julia_notebook2.png)

[Reference](https://datatofish.com/add-julia-to-jupyter/)

## Install FICO Xpress
1. Go to the [Xpress Community License application website](https://content.fico.com/xpress-optimization-community-license) and fill in your information to apply for a community license
2. Once submit, you'll be directed to a download page. Choose the **Xpress (Workbench, Mosel & Solver)** installation package that suits your operation system

![Xpress Download options](https://github.com/Pheobe-Sun/Julia-for-optimisation/blob/main/static/Install_Xpress.PNG)

3. Run the installation file once downloaded. Choose 'continue to install' or 'trust' this app on receipt of security warning
4. Installation begins. Click on 'setup' if prompted (see images [here (windows)](https://www.fico.com/fico-xpress-optimization/docs/latest/installguide/dhtml/chapinst1_sec_secwin.html))
5. Follow the instructions, choose the 'Community License' when asked
6. When you see the 'Choose Destination Location' page, make sure you know where Xpress is installed. The **path** will come handy for you at a later stage.
7. Tick the box “Yes, install the Xpress Kalis Mosel addon” when asked
8. Now you have installed Xpress. Let's **manually add the Xpress path (C:\xpressmp\bin) to the Windows environment path**
    - Control panel -> system -> advanced system settings -> system properties -> environment variables -> change system variables -> add XPRESSDIR\bin (see [here](https://learn.sparkfun.com/tutorials/configuring-the-path-system-variable/all) for step-by-step illustration)
    - **Restart your laptop**

## Install Xpress Wrapper 
*This wrapper allows you to use Xpress in your jupyter notebook*
1. Open Julia Command-Line (for Windows users, type 'Julia' in the windows search bar and then click on 'Julia 1.6.2')
2. Type in ``import Pkg`` and press Enter
3. Type in ``Pkg.add("Xpress")`` and press Enter. Wait for a while ([reference](https://github.com/jump-dev/Xpress.jl))
4. Type in ``Pkg.add("JuMP")`` and press Enter. Wait for a while ([reference](https://jump.dev/JuMP.jl/stable/installation/))
5. Type in ``Pkg.build("Xpress")`` and press Enter. Wait  for a while
6. Test if installed by typing ``using JuMP, Xpress``. If you see the return saying 'found lincense file', your Xpress is ready to use. 

![Xpress wrapper installation success](https://github.com/Pheobe-Sun/Julia-for-optimisation/blob/main/static/Install_success.PNG)

## Troubleshooting
