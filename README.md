# WIP : Jupyter + .NET Preview 1 documentation 

- [Getting started online](#online)
- [Getting started on your machine](#on-your-machine) 

# Online

We have provided two online experiences to get you started. 

- [Try our .NET Notebook](#try-jupyter--net)
- [Create your own Binder](#deploy---share-your-net-notebook-on-binder)

## Try Jupyter + .NET 

Requirement :  A browser

To get you started, we created a set of samples (C# and F#).  These samples have been designed to provide a zero-install experience, allowing you to try the .NET kernel setup free.

### Steps

- Click on the **launch binder** badge below. 

    [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/dotnet/try/master)

- This launches the binder service.

    ![Binder - Google Chrome 2019-10-08 19-48-33](https://user-images.githubusercontent.com/2546640/66441636-c9a0b780-ea05-11e9-9554-caf4fd7dfcde.gif)

-  Select one of the .NET folder options C# or F#
-  In the C# or F# folder you will find a Docs and a samples folder.
    - Docs folder - A how to guide that goes over formatting, plotting, magic commands etc. 
    ![image](https://user-images.githubusercontent.com/2546640/66443156-fb1c8180-ea0b-11e9-9a75-c9e8a0b415ab.png)

    - Samples folder - Contains a set of samples that you learn and experiment with. 
    ![image](https://user-images.githubusercontent.com/2546640/66443240-4b93df00-ea0c-11e9-8bf2-57dd9394e0af.png)

    - Select on the samples and start running the cells.
     
     *Please note the first cell might take a few seconds, since we are loading a few nuget packages*
        ![image](https://user-images.githubusercontent.com/2546640/66443801-7717c900-ea0e-11e9-89ce-00169c6b2815.png)

     - Now, you can run and edit the cells, import and plot data. 
     ![image](https://user-images.githubusercontent.com/2546640/66444711-45a0fc80-ea12-11e9-920c-d62dcd6fb365.png)
     ![image](https://user-images.githubusercontent.com/2546640/66444747-6b2e0600-ea12-11e9-8934-d352ed07b532.png)
     ![image](https://user-images.githubusercontent.com/2546640/66444785-89940180-ea12-11e9-8c98-4ce5c1dfc1a4.png)
     ![image](https://user-images.githubusercontent.com/2546640/66444810-a92b2a00-ea12-11e9-855f-c933d3367778.png)

## Deploy &  Share your .NET Notebook on [binder](https://mybinder.org/)

Requirements 
-  Git Repo
-  [Jupyter + .NET kernel installed](#on-your-machine) 

### Steps
- Step up a [Git Repo](https://help.github.com/en/articles/create-a-repo).
- Open a Terminal or Command prompt 
- Clone your new repo `git clone repo url`
- Switch to the repo directory 
- Start a new notebook
    `jupyter notebook` or `jupyter lab`
- Click new and select one of the .NET options C# or F#

    ![image](https://user-images.githubusercontent.com/2546640/66432173-70c42580-e9eb-11e9-895e-d08cb2f5c54d.png)    
- Rename your Notebook
    ![image](https://user-images.githubusercontent.com/2546640/66717693-ec3a2400-eda9-11e9-810d-099442c3e86c.png)
- Start writing up your notebook. 


# On your machine

### Installation 
- [**Getting started on Windows**](#windows)
- [**Getting started on macOS**](#macos)

## Windows 

Requirements
- [.NET 3.0 SDK](https://dotnet.microsoft.com/download)
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
## MacOS
Requirements
- [.NET 3.0 SDK](https://dotnet.microsoft.com/download)
- [Jupyter](https://jupyter.org/install) : JupyterLab can be installed using [Anaconda](https://www.anaconda.com/distribution) or  `conda` or `pip`. For more details on how to do this please checkout the [offical Jupyter installation](https://jupyter.org/install) guide.
    - *An alternative to using Anaconda to install Jupyter you could use Homebrew.*
    
        `brew install jupyter`

        `jupyter notebook`

### Install the .NET Kernel
- Open Terminal 
- Install the dotnet try global tool

    `dotnet tool install -g dotnet-try --add-source https://dotnet.myget.org/F/dotnet-try/api/v3/index.json`

*Please note: If you have the `dotnet try` global tool already installed, you will need to uninstall before grabbing the kernel enabled version of the dotnet try global tool.*

- Install the kernel 

    `dotnet try jupyter install`

    ![image](https://user-images.githubusercontent.com/2546640/66361692-a6b2cc80-e94d-11e9-913d-f6062d460cc9.png)

- Test installation 

    `jupyter kernelspec list`

    You should see the `.net-csharp`  and `.net-fsharp` listed.

    ![image](https://user-images.githubusercontent.com/2546640/66361581-4e7bca80-e94d-11e9-9312-1c672cba6596.png)

-  Start a notebook 

    `jupyter notebook`

    ![image](https://user-images.githubusercontent.com/2546640/66431857-d532b500-e9ea-11e9-9203-e5626fc3aa67.png)


- Click new and select one of the .NET options C# or F#

    ![image](https://user-images.githubusercontent.com/2546640/66432173-70c42580-e9eb-11e9-895e-d08cb2f5c54d.png)    

-  Now you can write .NET 
    ![image](https://user-images.githubusercontent.com/2546640/66432344-d9ab9d80-e9eb-11e9-9a88-cdd9a349b58f.png)



