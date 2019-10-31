 On your machine

### Installation 

Requirements
- [.NET 3.0 SDK](https://dotnet.microsoft.com/download) (follow the setup for your OS)
- [Jupyter](https://jupyter.org/install) : JupyterLab can be installed using [Anaconda](https://www.anaconda.com/distribution) or  `conda` or `pip`. For more details on how to do this please checkout the [offical Jupyter installation](https://jupyter.org/install) guide.

### Install the .NET Kernel
- Open Command Prompt or if you have Anaconda installed use Anaconda Prompt
- Install the dotnet try global tool

    `dotnet tool install -g dotnet-try --add-source https://dotnet.myget.org/F/dotnet-try/api/v3/index.json`

*Please note: If you have the `dotnet try` global tool already installed, you will need to uninstall before grabbing the kernel enabled version of the dotnet try global tool.*
- Check to see if jupyter is installed 

    `jupyter kernelspec list`
    
- Install the kernel 

    `dotnet try jupyter install`
    
    ![image](https://user-images.githubusercontent.com/2546640/63954737-93106e00-ca51-11e9-8c72-939f3f558d05.png)

- Test installation 

    `jupyter kernelspec list`

    You should see the `.net-csharp`  and `.net-fsharp` listed.

    [Insert Image here]
-  You can use either one the commands below to a start a notebook.  

    `jupyter notebook` - Starts Jupyter notebooks.

    Or
   
    `jupyter lab` - Starts [Jupyter Lab](https://blog.jupyter.org/jupyterlab-is-ready-for-users-5a6f039b8906)
- Click new and select one of the .NET options C# or F#

    ![image](https://user-images.githubusercontent.com/2546640/66432173-70c42580-e9eb-11e9-895e-d08cb2f5c54d.png)    

-  Now you can write .NET 
    ![image](https://user-images.githubusercontent.com/2546640/66432344-d9ab9d80-e9eb-11e9-9a88-cdd9a349b58f.png)

-  Start a notebook 

    `jupyter notebook`

    ![image](https://user-images.githubusercontent.com/2546640/66431857-d532b500-e9ea-11e9-9203-e5626fc3aa67.png)


- Click new and select one of the .NET options C# or F#

    ![image](https://user-images.githubusercontent.com/2546640/66432173-70c42580-e9eb-11e9-895e-d08cb2f5c54d.png)    

-  Now you can write .NET 
    ![image](https://user-images.githubusercontent.com/2546640/66432344-d9ab9d80-e9eb-11e9-9a88-cdd9a349b58f.png)
