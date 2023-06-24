[![Simulation](../../actions/workflows/main.yml/badge.svg)](../../actions/workflows/main.yml)

# Lesson 3 - Generators

The goal this lesson is to familiarize you with the various ways of modeling generators in GridLAB-D. The specific learning objectives are the following

1. How to define a diesel generator.
2. How to define a solar generator.
3. How to define a wind turbine.

## Generators

To define generators, you must include the `generators` module using the `module generators;` GLM directive.

Generators can be connected to any single phase or 3-phase nodes on a network. 

## Tasks

The following tasks are illustrated in [`main.glm`](main.glm):

1. Load the `generators` module (see [`main.glm@7`](main.glm#L7)).
1. Add a 1 cylinder, 2 stroke, 3-phase diesel generator running at 360 rpm, with 680 N of torque to `node_8` (see [`main.glm@8`](main.glm#L8-L19)).

# Exercises

1. Change the diesel generator to a single phase (A) connected to and with the same power as [`load_1`](https://github.com/arras-energy/gridlabd-models/blob/master/gridlabd-4/IEEE/123.glm#L411-L418). (Hint: $power = \frac{2 \pi}{60} \frac{rpm \times torque}{stroke \times cylinders}$).

# More Information

* [Generator Module](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Generators&doc=/Module/Generators/Diesel_dg.md)
    * [Diesel Generators](https://docs.gridlabd.us/_page.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Generators&doc=/Module/Generators/Diesel_dg.md)
    * [Solar Panels](https://docs.gridlabd.us/_page.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Generators&doc=/Module/Generators/Solar.md)
    * [Wind Turbines](https://docs.gridlabd.us/_page.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Generators&doc=/Module/Generators/Windturb_dg.md)
    * [Microturbines](https://docs.gridlabd.us/_page.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Generators&doc=/Module/Generators/Microturbine.md)

# Next Lesson

* [Lesson 4 - Generators](../../../lesson-4)
