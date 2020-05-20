# Erythromycin-Model
Whole-body PBPK model of erythromycin as CYP3A4 perpetrator drug

<a title="Erythromycin" href="https://commons.wikimedia.org/wiki/File:Erythromycin_A_skeletal.svg"><img width="256" alt="Erythromycin A skeletal" src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/3c/Erythromycin_A_skeletal.svg/256px-Erythromycin_A_skeletal.svg.png"></a>

This repository contains:

- a [PK-Sim snapshot (*.json) file](https://docs.open-systems-pharmacology.org/working-with-pk-sim/pk-sim-documentation/importing-exporting-project-data-models#exporting-project-to-snapshot-loading-project-from-snapshot) of the current PBPK model
- static content (e.g. text blocks, *.md files) as inputs for an evaluation plan
- an evaluation plan (evaluation-plan.json) to create an evaluation report using the snapshot and static text blocks to display the performance of the model

**The latest release of the snapshot of the model, the evaluation plan and the static content can be found [here](https://github.com/Open-Systems-Pharmacology/Erythromycin-Model/releases/latest).**

**The latest release of the PK-Sim project model file and the respective evaluation report can be found [here](https://github.com/Open-Systems-Pharmacology/OSP-PBPK-Model-Library/releases).**

This erythromycin model is intended to be used in the context of CYP3A4-mediated drug-drug interactions. 

The model features metabolism by CYP3A4, glomerular filtration, and a dummy clearance (technically implemented as hepatic plasma clearance) that accounts for additional clearance pathways, as well as mechanism-based inhibition of CYP3A4. The model has been developed using a broad range of clinical data reported in the literature for the following salt forms and formulation types:

- erythromycin lactobionate for intravenous (IV) administration
- erythromycin stearate in film-coated tablets for oral (PO) administration
- erythromycin as free base in enteric-coated tablets for oral (PO) administration
- erythromycin as free base in enteric-coated capsules containing pellets for oral (PO) administration

## Code of conduct

Everyone interacting in the Open Systems Pharmacology community (codebases, issue trackers, chat rooms, mailing lists etc...) is expected to follow the Open Systems Pharmacology [code of conduct](https://github.com/Open-Systems-Pharmacology/Suite/blob/master/CODE_OF_CONDUCT.md#contributor-covenant-code-of-conduct).

## Contribution

We encourage contribution to the Open Systems Pharmacology community. Before getting started please read the [contribution guidelines](https://github.com/Open-Systems-Pharmacology/Suite/blob/master/CONTRIBUTING.md#ways-to-contribute). If you are contributing code, please be familiar with the [coding standard](https://github.com/Open-Systems-Pharmacology/Suite/blob/master/CODING_STANDARDS.md#visual-studio-settings).

## License

The model code is distributed under the [GPLv2 License](https://github.com/Open-Systems-Pharmacology/Suite/blob/develop/LICENSE).
