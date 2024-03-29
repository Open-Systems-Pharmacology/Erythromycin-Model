The general workflow for building an adult PBPK model has been described by Kuepfer et al. ([Kuepfer 2016](#5-references)). Relevant information on the anthropometry (height, weight) was gathered from the respective clinical study, if reported. Information on physiological parameters (e.g. blood flows, organ volumes, hematocrit) in adults was gathered from the literature and has been incorporated in PK-Sim® as described previously ([Willmann 2007](#5-references)). The  applied activity and variability of plasma proteins and active processes that are integrated into PK-Sim® are described in the publicly available 'PK-Sim® Ontogeny Database Version 7.3' ([PK-Sim Ontogeny Database Version 7.3](#5-references)).

The PBPK model was developed based on clinical data of healthy adult subjects obtained from the literature, covering different formulation types and erythromycin salts. Multiple doses and dosing schedules following intravenous (IV) and oral (PO) administration were included in model building. Mass balance information on urinary excretion of unchanged erythromycin after IV administration was also accounted for during the model building process.

Unknown parameters were simultaneously optimized using all available PK data, in particular:

-  4 data sets following single IV administration of 4 different doses of erythromycin (125 mg, 250 mg, 300 mg, 500 mg) as erythromycin lactobionate
- 6 data sets following single and multiple PO administration of 3 different doses of erythromycin (250 mg, 500 mg, 1000 mg) as film-coated tablets containing erythromycin stearate
- 2 data sets following single PO administration of 500 mg erythromycin as enteric-coated tablets containing erythromycin as base
- 2 data sets following single and multiple PO administration of 2 different doses of erythromycin (250 mg, 500 mg) as enteric-coated capsules containing pellets of erythromycin as base

Structural model selection was mainly guided by visual inspection of the resulting description of data and biological plausibility. The following parameters were identified using the Parameter Identification module provided in PK-Sim® and MoBi® ([Open Systems Pharmacology Documentation](#5-references)):

- `Specific intestinal permeability (transcellular)`
- `Transport Protein - OATP1B1 - kcat`
- `Metabolizing Enzyme - CYP3A4 - kcat`
- `Total Hepatic Clearance - Specific clearance`
- `GFR fraction`
- `K_kinact_half` 
- `kinact` 
- `Dissolution shape` (separately for the film-coated tablet containing erythromycin stearate, the enteric-coated tablet containing erythromycin as base, and the enteric-coated capsule containing pellets of erythromycin as base)
- `Dissolution time (50% dissolved)` (separately for the film-coated tablet containing erythromycin stearate, the enteric-coated tablet containing erythromycin as base, and the enteric-coated capsule containing pellets of erythromycin as base)
- `Dissolution lag time` (separately for the enteric-coated tablet containing erythromycin as base and the enteric-coated capsule containing pellets of erythromycin as base)
- `Solubility at reference pH` (only for the enteric-coated tablet containing erythromycin as base)

Details about input data (physicochemical, *in vitro* and clinical) can be found in [Section 2.2](#22-data).

Details about the structural model and its parameters can be found in [Section 2.3](#23-model-parameters-and-assumptions).





