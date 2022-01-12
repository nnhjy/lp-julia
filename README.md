# Exercise for Course MS-E2121 - Linear Optimization D at Aalto University

## Installing Julia

We recommend that you install Julia on you own laptop or work computer. This way it is easy to continue using Julia after the course.

First, [download the current release of Julia](http://julialang.org/downloads/). For more details see [Julia's own installation instructions](https://julialang.org/downloads/platform/).

**Windows**: Run the installer. Then open the Julia application (double-click on it); a window with a julia> prompt will appear.

If you want to use WSL, check the instructions at the end.

**MacOS**: Open the dmg file and dragg the Julia app `Applications`. Run the application and a window with a julia> prompt will appear.

**Linux**: Open a terminal window and run the following commands to
download and extract the necessary files:

```bash
wget https://julialang-s3.julialang.org/bin/linux/x64/1.6/julia-1.6.5-linux-x86_64.tar.gz
tar zxvf julia-1.6.5-linux-x86_64.tar.gz
export PATH="$PATH:~/julia-1.6.2/bin"
```

To use Julia later, you will need to add the following line to the `.bashrc` file in your home folder.
```bash
export PATH="$PATH:~/julia-1.6.5/bin"
```

**All systems**:

Start a Julia session.
Install the `IJulia` package by pasting the following two:

```julia
using Pkg
Pkg.add("IJulia")
```
You may also want to install these packages, which we tend to use in a lot of the lecture materials
```julia
Pkg.add("Plots")
Pkg.add("Cbc")
Pkg.add("JuMP")
```

Then you can launch the notebook in your browser by running
```julia
using IJulia
notebook(dir=".")
```

The first time you run this, it will ask about installing Jupyter using conda.
Answer 'y' and after a while, the notebook environment will open in the
browser.
