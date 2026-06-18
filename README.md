# Multi-Locus Phylogenetic Analysis of *Fusarium* Isolates VMFi101 and VMFi102

This repository contains the multi-locus sequence analysis (MLSA) framework and phylogenetic datasets used to establish the taxonomic identity and evolutionary relationships of fungal isolates **VMFi101** and **VMFi102**. 

By concatenating three highly informative nuclear markers—the internal transcribed spacer (**ITS**) region, translation elongation factor 1-α (**TEF-1α**), and the RNA polymerase II largest subunit (**RPB2**)—we successfully resolved the phylogenetic placement of these isolates within the genus *Fusarium*.

---

## 📊 Project Overview & Summary
* **Target Isolates:** VMFi101, VMFi102
* **Molecular Markers:** ITS, TEF-1α, RPB2 (Concatenated)
* **Dataset Scale:** 31 Nucleotide Sequences | 4,921 Informative Positions
* **Taxonomic Outcome:** Robust identification as members of the ***Fusarium incarnatum*** species complex (FIESC).

---

## 🔬 Methodology

Evolutionary analyses and tree reconstructions were executed in **MEGA12** utilizing optimized parallel computing threads. The workflow followed a rigorous Maximum Likelihood (ML) framework:

1. **Sequence Alignment:** Nucleotide sequences from individual loci were aligned using MUSCLE and subsequently concatenated into a master multi-locus dataset.
2. **Heuristic Search Seeding:** * An initial tree was chosen by evaluating and comparing the log-likelihood scores of a Neighbor-Joining (NJ) topology and a Maximum Parsimony (MP) topology.
   * The NJ tree matrix of pairwise distances was computed using the **p-distance** model.
   * The MP tree was selected as the shortest topology resolved across **10 independent searches**, each initiated with a randomized starting tree.
3. **Phylogenetic Inference:** Maximum Likelihood inference was performed under the **Tamura-Nei (1993)** nucleotide substitution model. 
4. **Topology Validation:** Branch support and nodal stability were assessed using **100 bootstrap replicates**.

---

## 📈 Key Results

The finalized ML analysis yielded a stable topology with a highest log-likelihood score of **`-18,380.56`**.

### Phylogenetic Placement Highlights
* **Monophyletic VMFi Clade:** Isolates `VMFi101` and `VMFi102` clustered together with absolute bootstrap support (**100%**) into a unified terminal branch.
* **Placement within FIESC:** The VMFi sister pair nested cleanly within the ***Fusarium incarnatum*** species complex, positioning itself basal to the core reference subclade (`LC 13705`, `NRRL 13379`, `NRRL 32866`, and `NRRL 32867`). This divergence is supported by a **77%** node bootstrap value.
* **Macro-Systematics:** The tree robustly segregated neighboring lineages with high resolution, such as the *Fusarium oxysporum* complex (**100%** support) forming a sister relationship to the *Fusarium siculi* clade. Deeper nodes cleanly split the more distant complexes (*F. ensiforme*, *F. salinense*, *F. citricola*, and *F. sarcochroum*) with a basal support of **67%**.

---

## 🌳 Included Taxa & Species Complexes

The final multi-locus dataset encompasses 31 operational taxonomic units (OTUs):

| Species Complex | Included Strains / Accessions |
| :--- | :--- |
| **Query Isolates** | `VMFi101`, `VMFi102` |
| ***F. incarnatum*** | `LC_13705`, `NRRL_13379`, `NRRL_32866`, `NRRL_32867` |
| ***F. siculi*** | `CPC_27188`, `CPC_27189` |
| ***F. oxysporum*** | `CPC_27194`, `CPC_27196`, `CPC_27700`, `CPC_27701`, `CPC_27702`, `CPC_28190` |
| ***F. salinense*** | `CPC_26403`, `CPC_26457`, `CPC_26973` |
| ***F. citricola*** | `CPC_27067`, `CPC_27069`, `CPC_27709`, `CPC_27805`, `CPC_27813` |
| ***F. ensiforme*** | `CPC_27190`, `CPC_27191` |
| ***F. sarcochroum*** | `CPC_26369`, `CPC_26370`, `CPC_26851`, `CPC_27921`, `CPC_28075`, `CPC_28116`, `CPC_28118` |

---

## 🛠️ Reproducibility & iTOL Visualization

To visualize the tree layout using the standard publication-ready horizontal gradient color blocks:
1. Upload the Newick tree string to the **Interactive Tree Of Life (iTOL)** platform.
2. Drag and drop the companion annotation metadata file (`TREE_COLORS` block format) provided in this repository to automatically apply background shading across the species complexes.
3. In the iTOL control panel, toggle **Bootstraps/metadata** to **Text** to view the support scores next to the branches.

## 📄 References
* **Substitution Model:** Tamura K. and Nei M. (1993). *Molecular Biology and Evolution* 10:512-526.
* **Bootstrap Support:** Felsenstein J. (1985). *Evolution* 39:783-791.
* **MEGA12 Platform:** Kumar S., et al. (2024). *Molecular Biology and Evolution* 41:1-9.
