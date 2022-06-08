# Project Structure

1. PRISM-extended.tar.gz <--- source code of PRISM+

2. 13_nodes.prism <--- PRISM+ specification of the Casper Hybrid protocol with 13 nodes

3. properties.prop <--- list of the properties analyzed in the paper (PRISM syntax)

4. prob_safety.eps <--- results for the analysis of the accountable safety property

5. prob_liveness.eps <--- results for the analysis of the plausible liveness property


# Instructions for the installation of PRISM+

-> Download the PRISM-extended.tar.gz file and extract it

-> To install, enter the PRISM-new directory and type ./install.sh

-> To run, execute bin/xprism or bin/prism


# Docker

-> We also provide a docker image with our implementation, available at https://hub.docker.com/repository/docker/meivan/bitprism


# Instructions to run an experiment

-> To run an experiment from command line, it is possible to write:
```console
prism model.prism property -const -sim -simmethod ci
```
  where 
    * model.prism is the name of the file
    * property is the property to analyze (e.g. P=?[F<=T "someJustified"]) 
    * after const it is supposed to define the variables not initialized in the model, in our case the only variable not initialize is epochs
  For instance, if you want to analyze the probability that someone justifies a block depending on the number of epochs you should write:
```console
prism 13_nodes.prism P=?[F<=T "someJustified"] -const epochs=0:5:20 -sim -simmethod ci
```
