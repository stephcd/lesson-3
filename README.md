[![Simulation](../../actions/workflows/main.yml/badge.svg)](../../actions/workflows/main.yml)

# Lesson 3 - Generators

The goal this lesson is to familiarize you with the various ways of modeling generators in GridLAB-D. The specific learning objectives are the following

1. How to connect a diesel generator.
2. How to connect a solar generator.
3. How to connect a wind turbine.

## Generators

To define generators, you must include the `generators` module using the `module generators;` GLM directive.

Generators can be connected to any single phase or 3-phase nodes on a network. Some generators such as diesel generators can be directly connected to the network. Renewables resources such as wind and solar must be connected through meters. Some renewables, such as solar panels, must also be connected through inverters.

When a generator's output depends on weather, then the weather data and the time must be specified.

## Tasks

The following tasks are illustrated in [`main.glm`](main.glm):

1. Load the `generators` module (see [`main.glm@7`](main.glm#L7)).
2. Add a 1 cylinder, 2 stroke, 3-phase diesel generator running at 360 rpm with 680 N.m of torque to `node_8` (see [`main.glm@8`](main.glm#L8-L19)).
3. Add a 4 kW 100 sf solar panel with 13.5% efficiency titled at 45 deg facing south to `node_10` (see [`main.glm@21`](main.glm#L21-L55)).
   1. Get and load the weather data ([`main.glm@22`](main.glm#L22-L25)).
   2. Set the time to use for the weather data ([`main.glm@26`](main.glm#L26-L31)).
   3. Connect a meter to `load_10` ([`main.glm@32`](main.glm#L32-L54)).
   4. Connect an inverter to the meter ([`main.glm@39`](main.glm#L38-L53)).
   5. Connect the solar panel to the inverter ([`main.glm@46`](main.glm#L43-L52)).
4. Add a 100 kW generic small induction wind turbine to `load_28` (see [`main.glm@57`](main.glm#L56-L72)).
   1. Connect a meter to `load_28` ([`main.glm@57`](main.glm#L57-L72)).
   2. Connect the wind turbine to the meter ([`main.glm@57`](main.glm#L62-L71)).

# Exercises

1. Change the diesel generator to a single phase (A) connected to and with the same power as [`load_9`](https://github.com/arras-energy/gridlabd-models/blob/master/gridlabd-4/IEEE/123.glm#L465-L472). (Hint: $power = \frac{2 \pi}{60} \frac{rpm \times torque}{stroke \times cylinders}$).
2. Increase the size of the solar panel to 1000 sf, and increase the capacity of the panel and inverter to support the potential output of the panel.

# More Information

* [Generator Module](https://docs.gridlabd.us/index.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Generators&doc=/Module/Generators/Diesel_dg.md)
    * [Diesel Generators](https://docs.gridlabd.us/_page.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Generators&doc=/Module/Generators/Diesel_dg.md)
    * [Solar Panels](https://docs.gridlabd.us/_page.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Generators&doc=/Module/Generators/Solar.md)
    * [Wind Turbines](https://docs.gridlabd.us/_page.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Generators&doc=/Module/Generators/Windturb_dg.md)
    * [Microturbines](https://docs.gridlabd.us/_page.html?owner=arras-energy&project=gridlabd&branch=master&folder=/Module/Generators&doc=/Module/Generators/Microturbine.md)

# Next Lesson

* [Lesson 4 - Energy Storage](../../../lesson-4)
