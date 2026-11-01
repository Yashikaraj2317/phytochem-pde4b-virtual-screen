# Exploratory phytochemical screen: chronic bronchitis associated with COPD

## Status
Inputs prepared. Docking scores are NOT yet available. Empty score columns mean not run, not zero affinity.

## Target and positive control
Human PDE4B (UniProt Q07343), catalytic domain, PDB 1XMU chain A, 2.3 A X-ray structure.
Roflumilast is the positive control (PubChem CID 449193) and the crystallographic reference (CCD ROF).
Roflumilast is a PDE4-family inhibitor, not a PDE4B-selective control. This is an exploratory single-target screen; neither COPD efficacy nor PDE4B subtype selectivity can be concluded from it.
FDA indication: reduce exacerbation risk in severe COPD associated with chronic bronchitis and a history of exacerbations, not general treatment of all bronchitis.

## Library
50 unique, public-source phytochemicals plus 1 positive control. All 51 SMILES parse and have specified tetrahedral stereocentres where present. Source IDs, parent SMILES, source descriptions, descriptors and PAINS flags are in the accompanying table. This is a diversity-oriented hypothesis panel, not 50 proven PDE4B inhibitors. No compounds were excluded on drug-likeness or PAINS flags. RDKit PAINS flags occur for 22 entries and are warnings, not proof of assay interference.

## Receptor preparation
Keep chain A only; remove ROF and crystallographic waters (dry-pocket approximation); retain Zn1001 and Mg1002. Restore modified CME194 and CME432 to CYS with PDBFixer; closest crystal-ligand heavy-atom distances to the original CME residues are 21.690 and 5.608 A. No internal missing-residue gaps were observed in the resolved chain. Missing terminal OXT and hydrogens added at receptor pH 7.4. Do not reconstruct unresolved domain termini. Prepare rigid PDBQT with Meeko; both metals verified present. A prior Open Babel conversion failed and was discarded.

## Ligand-state limitation
Use PubChem parent SMILES exactly as retrieved, retaining their stereochemistry and formal charge (berberine +1). These are NOT validated physiological microstates. A Dimorphite-DL pH7.4 precision=0 run assigned implausible charges to polyphenols (quercetin -5 and EGCG -8), so that output was rejected. Acidic and polyphenolic top hits require a separate, validated protonation/tautomer sensitivity screen. Do not call parent-state results physiological-pH affinities.

## Initial docking settings
AutoDock Vina; identical settings for 50 candidates and roflumilast. Receptor rigid, ligands flexible. Center = (2.335346, 0.725346, 41.710923) A, the unweighted heavy-atom centroid of chain-A crystallographic ROF. Box 28 x 28 x 28 A. Exhaustiveness 32; up to 9 poses per ligand. Scores reported in kcal/mol as docking scores only. No calibrated Kd/Ki conversion.

## Validation and interpretation plan
Re-dock roflumilast from its SMILES and calculate symmetry-corrected heavy-atom pose RMSD to the saved crystal ligand without moving the receptor frame. Target RMSD <=2.0 A for the top-ranked pose; also report the best sampled pose RMSD. No pose-recovery success is claimed before this is computed. If recovery fails, do not use the ranking as validated evidence.
Rank successful ligands by their best Vina score, retain all failures explicitly, and report score(candidate)-score(roflumilast). Negative differences mean a more favourable score only, not experimentally stronger inhibition. Inspect interactions, clashes, ligand size bias, metal contacts and assay-interference flags. Vina does not rigorously model metal coordination, solvation or entropy. Small score differences are not reliable potency differences. Repeat docking of the leading candidates and test protonation states and key waters before prioritising experiments.
No experimentally verified negative-control ligand is included; do not label an arbitrary weak docking compound as a validated negative control. Later biochemical assays should include vehicle-only and no-enzyme controls, roflumilast, interference/aggregation counterscreens, and a PDE4D counter-assay for subtype selectivity.

## Public sources
- Structure: https://www.rcsb.org/structure/1XMU
- Protein: https://www.uniprot.org/uniprotkb/Q07343/entry
- Structure paper (abstract read): https://pubmed.ncbi.nlm.nih.gov/15576036/
- FDA labelling: https://dailymed.nlm.nih.gov/dailymed/drugInfo.cfm?setid=30dd6eae-6435-cae1-e063-6294a90a003b
- Positive control: https://pubchem.ncbi.nlm.nih.gov/compound/449193
- Per-compound PubChem links are in the library table; record descriptions were also retrieved through PubChem PUG View.

## Candidate list
- PHY01: Quercetin — PubChem 5280343; phytochemical
- PHY02: Kaempferol — PubChem 5280863; phytochemical
- PHY03: Luteolin — PubChem 5280445; phytochemical
- PHY04: Apigenin — PubChem 5280443; phytochemical
- PHY05: Myricetin — PubChem 5281672; phytochemical
- PHY06: Fisetin — PubChem 5281614; phytochemical
- PHY07: Isorhamnetin — PubChem 5281654; phytochemical
- PHY08: Morin — PubChem 5281670; phytochemical
- PHY09: Galangin — PubChem 5281616; phytochemical
- PHY10: Chrysin — PubChem 5281607; phytochemical
- PHY11: Baicalein — PubChem 5281605; phytochemical
- PHY12: Wogonin — PubChem 5281703; phytochemical
- PHY13: Scutellarein — PubChem 5281697; phytochemical
- PHY14: Naringenin — PubChem 439246; phytochemical
- PHY15: Hesperetin — PubChem 72281; phytochemical
- PHY16: Eriodictyol — PubChem 440735; phytochemical
- PHY17: Taxifolin — PubChem 439533; phytochemical
- PHY18: (+)-Catechin — PubChem 9064; phytochemical
- PHY19: (-)-Epicatechin — PubChem 72276; phytochemical
- PHY20: (-)-Epigallocatechin — PubChem 72277; phytochemical
- PHY21: (-)-Epicatechin gallate — PubChem 107905; phytochemical
- PHY22: (-)-Epigallocatechin gallate — PubChem 65064; phytochemical
- PHY23: Genistein — PubChem 5280961; phytochemical
- PHY24: Daidzein — PubChem 5281708; phytochemical
- PHY25: Formononetin — PubChem 5280378; phytochemical
- PHY26: Biochanin A — PubChem 5280373; phytochemical
- PHY27: Puerarin — PubChem 5281807; phytochemical
- PHY28: Resveratrol — PubChem 445154; phytochemical
- PHY29: Pterostilbene — PubChem 5281727; phytochemical
- PHY30: Curcumin — PubChem 969516; phytochemical
- PHY31: Caffeic acid — PubChem 689043; phytochemical
- PHY32: Ferulic acid — PubChem 445858; phytochemical
- PHY33: Sinapic acid — PubChem 10743; phytochemical
- PHY34: p-Coumaric acid — PubChem 637542; phytochemical
- PHY35: Rosmarinic acid — PubChem 5281792; phytochemical
- PHY36: Chlorogenic acid — PubChem 1794427; phytochemical
- PHY37: Ellagic acid — PubChem 5281855; phytochemical
- PHY38: Gallic acid — PubChem 370; phytochemical
- PHY39: Hydroxytyrosol — PubChem 82755; phytochemical
- PHY40: Oleuropein — PubChem 5281544; phytochemical
- PHY41: Carnosic acid — PubChem 65126; phytochemical
- PHY42: Carnosol — PubChem 442009; phytochemical
- PHY43: Ursolic acid — PubChem 64945; phytochemical
- PHY44: Oleanolic acid — PubChem 10494; phytochemical
- PHY45: Betulinic acid — PubChem 64971; phytochemical
- PHY46: Glycyrrhetinic acid — PubChem 10114; phytochemical
- PHY47: Berberine — PubChem 2353; phytochemical
- PHY48: Piperine — PubChem 638024; phytochemical
- PHY49: 6-Gingerol — PubChem 442793; phytochemical
- PHY50: 6-Shogaol — PubChem 5281794; phytochemical
- CTRL01: Roflumilast — PubChem 449193; positive_control
