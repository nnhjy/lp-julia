# Exercise for Course MS-E2121 - Linear Optimization D at Aalto University

## Installing Julia

We recommend that you install Julia on you own laptop or work computer. This way it is easy to continue using Julia after the course.

First, [download the current release of Julia](http://julialang.org/downloads/). For more details see [Julia's own installation instructions](https://julialang.org/downloads/platform/).

**Windows**: Run the installer. Then open the Julia application (double-click on it); a window with a julia> prompt will appear.

Change the julia executable to which the command `julia` points:
1. System environment variable (if you install Julia for all users):
"Control Panel\All Control Panel Items\System --> Advanced system settings --> Advanced --> Environmental Variables --> Edit in `Path`" 
    - under "User variables for `administrator_username`" only for the administrator, under "System variables" for all users)
2. User environment variable (if you install Julia for the current user): 
Search `environment variables` in the Windows taskbar --> "Edit environment variable for your account" --> Edit in `Path` under "User variables for `the_current_username`"
3. **Edit in `Path`**: Click `New` to add `X:\directory\to\Julia-x.x.x\bin` and delete the directory for old versions

*Check environment variables*: In `Command Prompt` type `path`. In normal mode, it shows the variables for the user, and in administrator mode the system variables.

If you want to use WSL, check the instructions at the end.

**Work with jupyter notebook**:

Start a Julia session.
Install the `IJulia` package by pasting the following two:

```julia
using Pkg
Pkg.add("IJulia")
```

Renew the julia kernel in notebook
```julia
using Pkg
Pkg.update()
Pkg.build("IJulia")
```

Then you can launch the notebook in your browser by running
```julia
using IJulia
notebook(dir=".")
```

The first time you run this, it will ask about installing Jupyter using conda.
Answer 'y' and after a while, the notebook environment will open in the
browser.
