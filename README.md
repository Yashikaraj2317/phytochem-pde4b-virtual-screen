# phytochem-pde4b-virtual-screen
Exploratory docking of 50 phytochemicals against human PDE4B (PDB 1XMU) with roflumilast as the control. Docking scores only, not validated affinities.
PDE4B phytochemical docking for chronic bronchitis/COPD

This repository holds an exploratory structure-based screen of 50 plant-derived compounds against human PDE4B, a target linked to chronic bronchitis associated with COPD. Roflumilast, an approved PDE4 inhibitor, is the positive control.

Target: human PDE4B (UniProt Q07343), PDB 1XMU chain A, with the catalytic Zn and Mg kept and waters removed.
Docking: AutoDock Vina, same box and settings for all compounds. Roflumilast re-docked to within 0.70 Å of its crystal pose.
Results: roflumilast scored −9.6 kcal/mol. Puerarin (−10.5), epicatechin gallate (−10.3) and biochanin A (−10.0) scored better. Theophylline (−6.4) and caffeine (−6.1) were run as weak references.
Interactions: the top phytochemicals sit much closer to the metal site than roflumilast, so their scores are probably inflated.
Limitations

Docking scores are not measured affinities and do not show PDE4B inhibition.
Differences under about 1 kcal/mol are within docking noise.
Ligands use PubChem parent forms, not validated pH 7.4 charge states.
Vina does not model metal coordination properly.
Metal-aware rescoring (Uni-GBSA or MD) has not been run.
There is no confirmed negative control.
