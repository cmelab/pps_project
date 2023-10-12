# pps_project
LSAMP project describing PPS using computational methods

1. MD sim of PPS morphology will be predicted using cmelab/jankflow to write
code based on hoomd to run a simulation.
2. Characterizing PPS by running several different amounts of molecules (N).
A plot will be created of TPS (timesteps per second) vs N.
TPS tells us how fast our simulation is progressing per second.
Number of PPS molecules will exponentially increase at a rate of e^10,
which will require help from Fry, a research computing cluster. This plot will
be written using matplotlib.
3. Run cmeutils function located in cmelab/cmelabutils/structure.py called
gsdRDF() and pass in a gsdfile of PPS simulated, bin_centers vs  RDF.RDF.
RDF curves tell us how likely at r we are to find a neighbor at that
distance. Dips tell us how unlikely we are to see a neighbor while peaks
tell us how likely we are to see a neighbor. As r approaches infinity, the 
RDF graph should level out at 1, as in a 3D space when a shell gets bigger,
it becomes infinitely more likely to find a nearby neighbor. Think of drawing
a sphere around a particular jellybean in a bathtub full of jellybeans. A
small sphere around that jelly bean will probably have only a few jelly beans
within the border of that sphere. As the sphere enlarges though, there will 
be sizes at which that sphere is very unlikely to encounter jellybeans. You
could think of this as the space in between the jellybeans. This is when a
dip on the RDF graph occurs. Inversely for the peaks.
