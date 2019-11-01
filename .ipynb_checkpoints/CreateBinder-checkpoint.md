# How to setup a my binder instance

If you want to share notebooks you have made using .Net kernels one easy way is to generate a binder image that everyone can open and execute.

You will need:

* **Dockerfile** to create the binder image
* **Nuget.Config** file to provide package source to use in notebooks
* Your notebooks

You can use the Dockerfile and Nuget.Config files from this repository to get started.

The repo file structure should look something like this.
![image](https://user-images.githubusercontent.com/375556/67017073-19137180-f0f1-11e9-9744-b5f8ec532e32.png)

The Dockerfile will install dotnet sdk
,then copy the notebooks and Nuget.config to folder under the notebook user

```docker
# Copy notebooks

COPY ./notebooks/ ${HOME}/notebooks/

# Copy package sources

COPY ./NuGet.config ${HOME}/nuget.config

RUN chown -R ${NB_UID} ${HOME}
USER ${USER}
```

Now push your changes to [github](https://github.com/).

Open a browser on [MyBinder homepage](https://mybinder.org/).

![image](https://user-images.githubusercontent.com/375556/67016428-16fce300-f0f0-11e9-98e7-d066ecb91049.png)

Put your repository url and branch
![image](https://user-images.githubusercontent.com/375556/67016633-66dbaa00-f0f0-11e9-8a6d-c7191de3142e.png)

Press launch to test your binder.

During development it is useful to use a commit hash so that you can even test different commits at the same time.

When happy with the result expand the section to reveal teh link and badge code so you can now embed it in your blogs and posts.

![image](https://user-images.githubusercontent.com/375556/67016821-bd48e880-f0f0-11e9-8c79-4fc97a06741a.png)
