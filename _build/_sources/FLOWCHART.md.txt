# How the Code Functions
This page contains a series of flow charts which describe how various modules and pipelines function. Module flow charts show how the classes perform their required functions, and pipeline flow charts show which modules are called within the pipeline. 

## Legend
The meanings of the different symbols used in the flow charts are defined below:

**Green Oval** - Start of module/pipeline
**Purple Hexagon** - Input
**Orange Hexagon** - Output
**Red Parallelogram** - CX-ASAP file
**Blue Rectangles - Plain** - Process or algorithm
**Blue Rectangles - Gradient** - Process imported from CX-ASAP
**White Double Rectangle** - External program
**White Diamond** - Decision made by CX-ASAP

## Modules

### ADP Analysis Module

![adp module](_static/module_adp_analysis.jpg)

### Cell Analysis Module

![cell analysis](_static/module_cell_analysis.jpg)

### CIF Merge Module

![CIF merge](_static/module_cif_merge.jpg)

### CIF Read Module

![CIF read](_static/module_cif_read.jpg)

### Instrument CIF Generation Module

![Instrument CIF](_static/module_instrument_cif_generation.jpg)

### Molecule Transformation Module

![Molecule Transformation](_static/module_molecule_transformation.jpg)

### PLATON Squeeze Module

![Squeeze](_static/module_platon_squeeze.jpg)

### Refinement Module

![Refinement](_static/module_cif_read.jpg)

### Rotation Planes Module

![Rotation](_static/module_rotation_planes.jpg)

### Structural Analysis Module

![Structural Analysis](_static/module_structural_analysis.jpg)

### XDS Cell Transformation Module

![XDS transformation](_static/module_xds_cell_transformation.jpg)

### XDS Reprocess Module

![XDS](_static/module_xds_reprocess.jpg)

### XPREP Module

![XPREP](_static/module_xprep.jpg)

### XPREP Intensity Comparison Module

![Intensity Comparison](_static/module_xprep_intensity_compare.jpg)

## Pipelines

### How Job Specific Pipelines Work

![how pipelines work](_static/overall_pipeline_general.jpg)


### CXASAP Pipeline (General)

![cxasap pipeline](_static/pipeline_general.jpg)

### Job Specific Pipeline 

![job specific pipeline](_static/job_specific_pipeline_general.jpg)

### Rigaku VT Pipeline

![rigaku](_static/pipeline_vt_rigaku.jpg)

### Variable Position Pipeline

![flexible mapping](_static/pipeline_flexible_mapping.jpg)

### Variable Temperature Pipeline (Australian Synchrotron)

![AS VT](_static/pipeline_vt_synchrotron.jpg)

