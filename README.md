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
