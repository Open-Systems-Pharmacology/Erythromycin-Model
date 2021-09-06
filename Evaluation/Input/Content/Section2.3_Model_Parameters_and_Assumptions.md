### 2.3.1	Dissolution and absorption

Development of an adequate absorption model for erythromycin was complicated by the large intersubject variability in the absorption kinetics of erythromycin ([Chun 1977](#5-References), [Mather 1981](#5-References)). Additionally, multiple formulation types are available entailing different dissolution and absorption kinetics ([Chun 1977](#5-References), [Yakatan 1980](#5-References), [Mather 1981](#5-References)). The herein presented model was developed for the following oral dosage forms:

- film-coated tablets containing erythromycin stearate
- enteric-coated tablets containing erythromycin as free base
- enteric-coated capsules containing pellets of erythromycin as free base

The following sections briefly address how each of these formulations was modeled in presented PBPK models.

#### 2.3.1.1	Film-coated tablet containing erythromycin stearate

Comparison of the reported erythromycin PK following administration of different doses of film-coated tablets containing the stearate salt indicated that the lowest dose - 250 mg - yields a larger t<sub>max</sub> than the higher doses (500, 1000 and 1500 mg). Different dissolution kinetics were therefore used for this formulation type; relatively slow dissolution kinetics was used for the 250 mg dose, whereas dissolution of the higher doses (500, 1000 and 1500 mg) was described by immediate-release kinetics. Both types of dissolution kinetics were described by the Weibull function. The parameters `Dissolution shape` and `Dissolution time (50% dissolved)` were optimized to optimally describe the clinical data. Additionally, solubility was also optimized as it was found during model building that solubility-limited absorption of the high doses better captured the observed PK profiles. 

#### 2.3.1.2	Enteric-coated tablet containing erythromycin as free base

Relatively few PK data were available for enteric-coated tablets containing erythromycin as free base. For this formulation type, PK profiles were only available for the 250 mg and 500 mg dose. For these two doses, dissolution was described by the Weibull function. To account for the enteric coating (protecting the tablet from dissolving in the stomach), a `lag time` > 0 min was applied in the model. To optimally describe the clinical data, relevant parameters of the Weibull function were optimized, namely the `Dissolution shape`, `Dissolution time (50% dissolved)` and `lag time`. Similar to the film-coated tablet containing the stearate salt, it was found that the observed PK profiles of the enteric-coated tablet containing erythromycin as free base could be better described when optimizing solubility. 

#### 2.3.1.3	Enteric-coated capsule containing pellets of erythromycin as free base

Comparison of the reported erythromycin PK following administration of different doses of enteric-coated capsules containing pellets of erythromycin base showed large variability in C<sub>max</sub> and t<sub>max</sub> both within and between different doses (dose range: 250 mg - 1000 mg). Here, dissolution kinetics was also described by the Weibull function with relevant parameters (`Dissolution shape`, `Dissolution time (50% dissolved)` and `lag time`) being optimized to better describe clinical data. However, optimizing solubility did not result in a better description of the observed PK profiles. Consequently, solubility of erythromycin in this formulation type was fixed to a high value (500 mg/L) to avoid any solubility-related limitations in dissolution and absorption.



For all three formulations, the same `Specific intestinal permeability (transcellular)` was used in the PBPK model. This parameter was also optimized to better describe the clinical PK data.

### 2.3.2	Distribution

With an average fraction unbound in human plasma of approximately 0.30, erythromycin is moderately protein-bound. In the developed model, the `fraction unbound (plasma, reference value)` was set to 0.305 which is the value reported by Barre et al. ([Barre 1987](#5-References)). `Lipophilicity` was fixed to a value of 2.82 which is the average of three experimentally measured values reported in the literature ([Lien 1974](#5-References), [Capobianco 1994](#5-References), [McFarland 1997](#5-References)). The observed PK data were found to be best described using the model for estimating intracellular-to-plasma partition coefficients according to the method by `Rodgers and Rowland` ([Rodgers 2005](#5-References), [Rodgers 2006](#5-References)). Cellular permeabilities were automatically calculated using the method `Charge dependent Schmitt`  ([Open Systems Pharmacology Documentation](#5-References)). Active transfer of erythromycin by OATP1B1 was modeled as Michaelis-Menten kinetics using an `Influx` transporter type; the `Km` value of 13.2 µM was taken from the literature ([Lancaster 2012](#5-References)) and `kcat` was optimized to best match observed clinical data. The gene expression profile of OATP1B1 (default symbol for the gene: LST-3TM12) was loaded from the internal PK-Sim® database using the expression data quantified by RT-PCR ([Open Systems Pharmacology Documentation](#5-References)). 

### 2.3.3	Elimination

Erythromycin is extensively metabolized via N-demethylation catalyzed by CYP3A. Kinetics of this biotransformation was described by a Michaelis-Menten process. The following kinetic parameters erythromycin N-demethylation have been measured in human liver microsomes (HLM) and reported in the literature (mean ± standard error):

| Vmax [nmol/min/mg mic protein] | Km [µM] | Microsomal preparation | Reference                    |
| ------------------------------ | ------- | ---------------------------- | ---------------------------- |
| 2 ± 0.09                       | 78 ± 9  | HLM from donor HL 3926 | [Wang 1997](#5-References)  |
| 0.41 ± 0.02                    | 44 ± 7  | HLM from donor HL 24493 | [Wang 1997](#5-References)  |
| 0.345 ± 0.013     | 88 ± 10 | mixed HLM pool | [Riley 1997](#5-References) |

In the PBPK model, `Vmax` and `Km` were fixed to the mean of the values tabulated above (70 µM and 0.918 nmol/min/mg mic protein). The gene expression profile of CYP3A4 was loaded from the internal PK-Sim® database using the expression data quantified by RT-PCR ([Open Systems Pharmacology Documentation](#5-References)).

Although it has also been observed that erythromycin is metabolized via CYP4F11 *in vitro* ([Kalsotra 2004](#5-References)), this elimination pathway was not accounted for in the model because its contribution to overall elimination was assumed to be low. In humans, CYP4F11 is mainly expressed in the liver and to a much lesser extent in the kidney ([Cui 2000](#5-References)) and the CYP4F family makes up approximately 15% of all hepatic CYP enzymes ([Michaels 2014](#5-References)). The K<sub>m</sub> and V<sub>max</sub> values for the CYP4F11-mediated biotransformation reported by [Kalsotra 2004](#5-References) are similar to those measured for CYP3A4 ([Riley 1997](#5-References), [Wang 1997](#5-References)), suggesting that the relative mass balance of these two metabolism pathways mainly depends on the absolute amount of each enzyme in the liver. While no information on total CYP4F11 in the human liver could be found in the literature, CYP4F11 expression in the liver of cynomolgus monkeys was observed to be approximately 6-fold lower than that of CYP3A4 ([Uehara 2015](#5-References)). Hence, it was assumed that CYP4F11-mediated metabolism of erythromycin can be neglected in humans.

Additional elimination pathways suggested for erythromycin are acid-catalyzed degradation (hydrolysis) the acidic milieu of the stomach ([Mordi 2000](#5-References)) and biliary excretion ([Acocella 1968](#5-References), [Chelvan 1979](#5-References)), but no quantitative information on the mass balance of these pathways could be found in the literature. Additionally, mechanism-based inhibition of CYP3A4 by erythromycin might constitute another clearance process which was neither considered in the model. However, a `total hepatic clearance` process was implemented in the model which could at least partly account for other elimination pathways not explicitly accounted for in the model. Of note, despite the name `total hepatic clearance`, this clearance pathway was implemented as dummy clearance accounting for additional elimination processes that are not covered by CYP3A-mediated clearance and unchanged renal excretion and it should hence rather be regarded as a partial than a total clearance. 

The reported dose fractions of erythromycin undergoing unchanged renal excretion after IV administration range from 0.018 ± 0.005 to 0.171 ± 0.11 (mean ± SD) ([Pasic 1987](#5-References), [Austin 1980](#5-References)). This information was accounted for in the model by implementing a glomerular filtration process and optimizing the `GFR fraction` to match the observed dose fractions excreted unchanged in urine.

### 2.3.4 Autoinhibition

In the scientific literature, large ranges have been reported for K<sub>I</sub> and k<sub>inact</sub> ([Section 2.2.2](#222in-vitro-data-on-mechanism-based-inhibition-of-cyp3a)). Since the exact values are unknown,  `K_kinact_half` and `kinact` were both optimized within the observed range (see [Section 2.2.2](#222in-vitro-data-on-mechanism-based-inhibition-of-cyp3a)) during model building to best match the observed clinical data. 

To better inform optimization of these two parameters, clinical data of a midazolam-erythromycin interaction study conducted by Olkkola et al. ([Olkkola 1993](#5-References)) were included in the parameter optimization during model building. Therefore, the midazolam PBPK model v0.9 available on OSP GitHub (https://github.com/Open-Systems-Pharmacology/Midazolam-Model/releases/tag/0.9) was loaded in the PK-Sim® erythromycin file and the study by Olkkola et al. ([Olkkola 1993](#5-References)) was simulated. However, instead of using the reported midazolam plasma concentrations as observed data in the parameter identification, the AUC of midazolam was used. More specifically, a midazolam target AUC after IV and oral administration was calculated by multiplying the simulated midazolam AUC (24.3 and 54.0 µmol min/L and after IV and oral administration, respectively) with the observed geometric mean AUC ratio (1.96 and 4.07 after IV and PO administration, respectively) ([Olkkola 1993](#5-References)) resulting in target AUCs of 47.4 and 220 µmol min/L after IV and oral administration of midazolam, respectively. These values were included as observed data values in the parameter identification during model building. Since the AUC is not a default output that can directly be used in the parameter identification, the PBPK model structure was modified prior to running the parameter identification as described in the following. After exporting the model to MoBi®, an artificial reaction of a dummy molecule was created. The reaction rate was defined as the simulated peripheral venous blood plasma concentration of midazolam, hence yielding the AUC at any specific time point. Thereafter, the model was imported in PK-Sim® and included in the parameter identification. After being used in the parameter identification during model building, the model was not used any further. 

### 2.3.5 Automated Parameter Identification

This is the result of the final parameter identification:

| Model Parameter                     | Formulation type/salt form               | Optimized Value  | Unit   |
| ----------------------------------- | ---------------------------------------- | ---------------- | ------ |
| `Dissolution shape `                | Enteric coated pellets                   | 1.0564916105     |        |
| `Dissolution shape `                | Enteric coated tablet                    | 1.0838799888     |        |
| `Dissolution shape `                | Filmcoated tablet (except 250 mg dose)   | 1.0960212213     |        |
| `Dissolution shape `                | Filmcoated tablet, 250 mg                | 3.2811974117     |        |
| `Dissolution time (50% dissolved) ` | Enteric coated pellets                   | 1.7462743767     | min    |
| `Dissolution time (50% dissolved) ` | Enteric coated tablet                    | 79.6337524677    | min    |
| `Dissolution time (50% dissolved) ` | Filmcoated tablet (except 250 mg dose)   | 1.7038947098     | min    |
| `Dissolution time (50% dissolved) ` | Filmcoated tablet, 250 mg                | 83.6562552486    | min    |
| `GFR fraction`                      |                                          | 1.1591081815     |        |
| `K_kinact_half` (CYP3A4)            |                                          | 7.6007360452     | µmol/L |
| `kcat` (OATP1B1)                    |                                          | 2.0201069202     | 1/min  |
| `kinact` (CYP3A4)                   |                                          | 0.0296261146     | 1/min  |
| `Km` (OATP1B1)                      |                                          | 0.735836485      | µmol/L |
| `Lag time`                          | Enteric coated pellets                   | 54.3490442506    | min    |
| `Lag time`                          | Enteric coated tablet                    | 78.7967495765    | min    |
| `Solubility at ref pH`              | Enteric coated tablet, erythromycin base | 8.3990771997     | mg/L   |
| `Solubility at ref pH`              | Filmcoated tablet, erythromycin stearate | 28.0708790976    | mg/L   |
| `Specific clearance`                |                                          | 4.1462183378     | 1/min  |
| `Specific intestinal permeability`  |                                          | 0.00038668371665 | cm/min |

<sup>*</sup> The value was set to 1.350032201 /min with the release of PK-Sim 10 to account for the updated calculation method of interstitial concentrations (please refer to the respective [release notes of version 10](https://github.com/Open-Systems-Pharmacology/Suite/releases/tag/v10)).