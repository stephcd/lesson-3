[![Simulation](../../actions/workflows/main.yml/badge.svg)](../../actions/workflows/main.yml)

# Lesson 3 - Generators

The goal this lesson is to familiarize you with the various ways of modeling generators in GridLAB-D. The specific learning objectives are the following

1. How to define a diesel generator.
2. How to define a solar generator.
3. How to define a wind turbine.

## Generators

Loads can be connected to either single phase or 3-phase nodes on a network.

## Tasks

The following tasks are illustrated in [`main.glm`](main.glm):

1. Add a 1 cylinder, 2 stroke, 3-phase diesel generator running at 360 rpm, with 680 N of torque to `node_8`.

# Exercises

1. Change the diesel generator to a single phase (A) with the same power as `load_1`. (Hint: $power = 2 \pi frac{rpm \times torque}{60 \times stroke \times cylinders}$)
2. 

# More Information

* [Generator Module](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Generators&doc=/Module/Generators/Diesel_dg.md)
    * [Diesel Generators](https://docs.gridlabd.us/_page.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Generators&doc=/Module/Generators/Diesel_dg.md)
    * [Solar Panels](https://docs.gridlabd.us/_page.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Generators&doc=/Module/Generators/Solar.md)
    * [Wind Turbines](https://docs.gridlabd.us/_page.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Generators&doc=/Module/Generators/Windturb_dg.md)
    * [Microturbines](https://docs.gridlabd.us/_page.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Generators&doc=/Module/Generators/Microturbine.md)

# Next Lesson

* [Lesson 4 - Generators](../../../lesson-4)