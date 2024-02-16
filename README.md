# mojo

### high-level: 
- systems programming and metaprogramming

### low-level: get the code running 
https://docs.modular.com/mojo/

configuring mojo SDK (https://developer.modular.com/download)

config done:
1. docker desktop
   - container: e.g. `docker run -d -p 80:80 docker/getting-started`
2. Mojo VSCode extension
3. Docker VSCode Dev Container extension
4. in project: tried Open a Remote Window -> New Dev Container --> `error: make sure the docker daemon is running`.

error log:
```bash
[7169166 ms] Dev Containers 0.338.1 in VS Code 1.86.2 (903b1e9d8990623e3d7da1df3d33db3e42d80eda).
[7169165 ms] Start: Run: docker version --format {{json .}}
[7169220 ms] Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running?

[7169221 ms] {"Client":{"CloudIntegration":"v1.0.35+desktop.10","Version":"25.0.3","ApiVersion":"1.44","DefaultAPIVersion":"1.44","GitCommit":"4debf41","GoVersion":"go1.21.6","Os":"darwin","Arch":"amd64","BuildTime":"Tue Feb  6 21:13:26 2024","Context":"default"},"Server":null}
[7169224 ms] Exit code 1
[9250074 ms] Start: Run: docker version --format {{json .}}
[9250129 ms] Cannot connect to the Docker daemon at unix:///var/run/docker.sock. Is the docker daemon running?

[9250130 ms] {"Client":{"CloudIntegration":"v1.0.35+desktop.10","Version":"25.0.3","ApiVersion":"1.44","DefaultAPIVersion":"1.44","GitCommit":"4debf41","GoVersion":"go1.21.6","Os":"darwin","Arch":"amd64","BuildTime":"Tue Feb  6 21:13:26 2024","Context":"default"},"Server":null}
[9250134 ms] Exit code 1
```

todo:
   - gotta get the right container running (search the error)
   - check if mojo project config is good or if i need to git clone



 Instead of downloading the Mojo SDK, you can also experiment with Mojo in our hosted Jupyter notebook environment called Mojo Playground. This is a hosted version of JupyterLab that’s running our latest Mojo kernel.

 The number of vCPU cores available in your cloud instance may vary,

 If you want to keep any edits to the included notebooks, rename the notebook files. These files will reset upon any server refresh or update, sorry. So if you rename the files, your changes will be safe.

You can use `%%python` at the top of a notebook cell and write normal Python code. Variables, functions, and imports defined in a Python cell are available for access in subsequent Mojo cells.

The Mojo environment does not have network access, so you cannot install other tools or Python packages. However, we’ve included a variety of popular Python packages, such as `numpy`, `pandas`, and `matplotlib` (see how to import Python modules - link).

Redefining implicit variables is not supported (variables without a let or var in front). If you’d like to redefine a variable across notebook cells, you must introduce the variable with var (let variables are immutable).

You can’t use global variables inside functions—they’re only visible to other global variables.

For a longer list of things that don’t work yet or have pain-points, see the Mojo roadmap and sharp edges.

You must set the `MODULAR_HOME` and `PATH` environment variables, as described in the output when you ran modular install mojo. For example, if you’re using bash or zsh, add the following lines to your configuration file (`.bash_profile`, `.bashrc`, or `.zshrc`):

```bash
export MODULAR_HOME="$HOME/.modular"
export PATH="$MODULAR_HOME/pkg/packages.modular.com_mojo/bin:$PATH"
```

Then source the file you just updated, for example:

`source ~/.bash_profile`

`PATH`: Specifies directories where executable programs are located.
`HOME`: Specifies the user's home directory.
`TEMP` or `TMP`: Specifies the directory for temporary files.
`USERNAME`: Specifies the currently logged-in user's username.
`LANG`: Specifies the language and localization settings.


