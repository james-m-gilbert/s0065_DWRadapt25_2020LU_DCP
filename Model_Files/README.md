# CalSim 3 | Climate Change Adaptation Analysis

This repository serves as the public source code repository of the [CalSim 3](https://water.ca.gov/Library/Modeling-and-Analysis/Central-Valley-models-and-tools/CalSim-3) model used in the [Climate Change Adaptation Analyses]() (DCR). 

CalSim 3 is an ever-evolving model, which changes with the updated regulatory, physical and operational considerations associated with California's water resources. This model is a cumulation of knowledge and inputs from a broad audience: DWR, the [United States Bureau of Reclamation](https://www.usbr.gov/), consultants, water users and academic institutions have contributed to this model. By sharing the source code on GitHub, we aim to continue (and introduce efficiencies to) this long-standing collaborative effort.

This code in this repository contains the WRESL code, lookup tables, initial [DSS](https://www.hec.usace.army.mil/software/hec-dssvue/) file and the required DLL's. No SV (State Variable) DSS files (inputs or outputs) are included to maintain repository fluidity. 
Necessary input .dss files (SV file) are maintained and stored on a separate Input Data Repository, hosted on Box.

# Dependencies
## Latest SV Files

The hydrology used by the DCR is linked in the table below.

[Danube CCA CHANGELOG](https://cawater.sharepoint.com/:p:/r/sites/dwr-callite/Shared%20Documents/SWP%20Climate%20Adaptation%20Plan/CalSim%203%20models/scenario_inputs/CCA_Changelog.pptx?d=wb7d0e424377c41babb3bf7e7d1d51479&csf=1&web=1&e=C6Rtkv)

| Planning Horizon | Latest SV      | Created On |
|------------------|:--------------:|:----------:|
|Historical        |[Version 1.7](https://cadwr.box.com/s/r4pauw0prvgkk9n4pp297880erzw6qcy)| 2024-07-03 |
|Adjusted          |[Version 1.8](https://cadwr.box.com/s/mca2mrzrq15ezh377gyztqayj8hsxmuh)| 2024-07-03 |
|CC50              |[Version 1.8](https://cadwr.box.com/s/rsvn0rm78u9ng7c5b75rn4aiy4q5ajwp)| 2024-07-03 |
|CC75              |[Version 1.8](https://cadwr.box.com/s/hm2vbg0w5ho69ytkweuto5v5zuab7pvh)| 2024-07-03 |
|CC95              |[Version 1.8](https://cadwr.box.com/s/0xql8s4wm4y60vwg70xis84df6czn41d)| 2024-07-03 |

## WRIMS
The latest code base uses an updated forecast DLL, which requires an updated version of WRIMS to run:
[WRIMS GUI 20240129](https://data.cnra.ca.gov/dataset/0f6b03b4-7de8-4579-8aa0-60f73d9d21fb/resource/b1c97752-d3ae-4fa1-bb67-8eed3d732c72/download/wrims2_gui_x64_20240129_fullpackage.zip)

![Image of WRIMS Software Icon](https://water.ca.gov/-/media/DWR-Images/DWR-Website-banners-Final/Library/WRIMS-2.jpg)
