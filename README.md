This piece of code generates PYTHIA8 events and writes an HepMC3 ROOT file as output. 

The simple compilation script makes use of the ALICE O2 installation to find and use the needed libraries. Otherwise the location of PYTHIA8 and HepMC3 libraries must be explicitly given. 

Two .cmnd files are meant for MB pp and centrality-selected Pb-Pb (centrality selection tuneable in the .cmnd itself). When asking for Pb-Pb collisions, Angantyr is called. 
A further .cmnd file produces a J/psi at each event and can be used to parameterize its distributions.

The code is launched by (for example) ./GenPYTHIA --events 100 --energy 150 --ymin -0.5 --ymax 0.5 --cmnd pp_MB.cmnd

In addition to the HepMC3 ROOT file it produces several histograms that may be useful for tuning of the PYTHIA parameters.
