📖 **Table of contents**
* [Predictors](#Predictors)
* [Tools and Extensions](#Tools)
* [Datasets and Databases](#Databases)
* [Webservers](#Webservers)


💡 **Notes**
- The following lists are curated by humans, as such may be incomplete
- We only include software targeting the folding problem combining learnings from AlphaFold 2 and protein language models. You may find other ML on protein tools [at Kevin's incredible ML for proteins list](https://github.com/yangkky/Machine-learning-for-proteins).
- We do not wish to advertize one tool over any other, but simply list the tools we are aware of in either random or alphabetical order
- Any suggestions for improvements and additions are welcome as issues or pull requests
- Projects we identify as discontinued are marked with 💀

⚡️ **Brought to you by:** 
- [@sacdallago](https://twitter.com/sacdallago)
- [@sokrypton](https://twitter.com/sokrypton)

----

<a name="Predictors"></a>
### Predictors
[_in alphabetical order_]
- **MSA-based** (uses Multiple Sequence Alignment as input)
  - AlphaFold2 (JAX) - OG
    - Manuscript: https://www.nature.com/articles/s41586-021-03819-2
    - Code: https://github.com/deepmind/alphafold
    - Other: [Colab Notebook](https://colab.research.google.com/github/deepmind/alphafold/blob/main/notebooks/AlphaFold.ipynb)
  - ColabFold (JAX) - faster AF2 compiling and MSA generations
    - Manuscript: https://www.nature.com/articles/s41592-022-01488-1
    - Code: https://github.com/sokrypton/ColabFold
    - Code: https://github.com/YoshitakaMo/localcolabfold
  - FastFold (Pytorch) - runtime improvements to OpenFold (see below)
    - Manuscript: https://arxiv.org/abs/2203.00854
    - Code: https://github.com/hpcaitech/FastFold
  - HelixFold (PaddlePaddle) - reimplements AF2 in PaddlePaddle
    - Manuscript: https://arxiv.org/abs/2207.05477
    - Code:  https://github.com/PaddlePaddle/PaddleHelix/tree/dev/apps/protein_folding/helixfold
  - MindSpore-Fold (mindspore) - reimplements AF2 in MindSpore
    - Manuscript: https://arxiv.org/abs/2206.12240
    - Code: https://gitee.com/mindspore/mindscience/tree/master/MindSPONGE/applications/MEGAProtein
  - OpenFold (PyTorch) - reimplements AF2 in PyTorch; provides training code and new model params
    - Manuscript: N/A
    - Code: https://github.com/aqlaboratory/openfold
    - Other: [Colab Notebook](https://colab.research.google.com/github/aqlaboratory/openfold/blob/main/notebooks/OpenFold.ipynb)
  - RoseTTAFold (PyTorch) - reproduction attempt of AF2 in PyTorch, before details of AF2 were available; new model params
    - Manuscript: https://www.science.org/doi/10.1126/science.abj8754
    - Code: https://github.com/RosettaCommons/RoseTTAFold
    - Other: [Unofficial Colab Notebook](https://colab.research.google.com/github/sokrypton/ColabFold/blob/main/RoseTTAFold.ipynb)
  - Uni-Fold (PyTorch/JAX) - reimplements AF2 in PyTorch; provides training code and new (monomer/multimer) model params
    - Manuscript: https://doi.org/10.1101/2022.08.04.502811
    - Code (PyTorch): https://github.com/dptech-corp/Uni-Fold
    - Code (JAX): https://github.com/dptech-corp/Uni-Fold-jax
  - 💀 Lucidrains' AlphaFold2 (PyTorch) - AF2 reproduction attempt
    - Code: https://github.com/lucidrains/alphafold2
  - 💀 Lupoglaz's OpenFold2 (PyTorch) - AF2 reproduction attempt
    - Code: https://github.com/lupoglaz/OpenFold2

- **pLM-based** (uses Protein Language Model as input)
  - ESM-Fold (PyTorch)
    - Manuscript: https://doi.org/10.1101/2022.07.20.500902
    - Code: N/A
    - Other: [[tweet] Alex's announcement](https://twitter.com/alexrives/status/1550148755206414341), 
  - EMBER3D (PyTorch):
    - Manuscript: N/A
    - Code: https://github.com/kWeissenow/EMBER3D
  - HelixFold-single (PaddlePaddle)
    - Manuscript: https://arxiv.org/abs/2207.13921
    - Code: https://github.com/PaddlePaddle/PaddleHelix/tree/dev/apps/protein_folding/helixfold-single
    - Resource: https://paddlehelix.baidu.com/app/drug/protein-single/forecast
  - IgFold (PyTorch) - specific to antibody sequences
    - Manuscript: https://www.biorxiv.org/content/10.1101/2022.04.20.488972v2
    - Code: https://github.com/Graylab/IgFold
    - Other: [Colab Notebook](https://colab.research.google.com/github/Graylab/IgFold/blob/main/IgFold.ipynb)
  - OmegaFold (PyTorch)
    - Manuscript: https://doi.org/10.1101/2022.07.21.500999
    - Code: https://github.com/HeliXonProtein/OmegaFold
    - Other:
      - [Unofficial Colab Notebook](https://colab.research.google.com/github/sokrypton/ColabFold/blob/main/beta/omegafold.ipynb)
      - [[tweet] Martin comparing structures](https://twitter.com/thesteinegger/status/1554881669718573062)
      - [[tweet] Sergey's positional encoding observation](https://twitter.com/sokrypton/status/1555536325176168448), 

<a name="Tools"></a>
### Tools and Extensions
  - gget (AF2)
    - Manuscript: https://doi.org/10.1101/2022.05.17.492392
    - Code: https://github.com/pachterlab/gget#gget-alphafold-
  - alphafold_finetune - finetune AlphaFold for Protein-Peptide prediction
    - Manuscript: https://www.biorxiv.org/content/10.1101/2022.07.12.499365v1
    - Code: https://github.com/phbradley/alphafold_finetune
    - Other: [[tweet] Amir's announcement](https://twitter.com/AMotmaen/status/1547435940011945984)
  - AlphaPulldown - protein-protein interaction screens using AlphaFold-Multimer
    - Manuscript: https://www.biorxiv.org/content/10.1101/2022.08.05.502961v1
    - Code: https://www.embl-hamburg.de/AlphaPulldown/
  - ColabDesign - Backprop through AlphaFold for protein design
    - Code: https://github.com/sokrypton/ColabDesign
  - AF2Rank - Rank Decoy Structures/Sequences using AlphaFold
    - Manuscript: https://www.biorxiv.org/content/10.1101/2022.03.11.484043v3
    - Code: https://github.com/jproney/AF2Rank
    - Resource: [Colab Notebook](https://colab.research.google.com/github/sokrypton/ColabDesign/blob/main/af/examples/AF2Rank.ipynb)
   
---- 
<a name="Databases"></a>
### Datasets for training
  - [OpenFold](https://registry.opendata.aws/openfold/) - MSAs for 132K PDBs + 270K UniClust30 predictions for distilation
  - [MindSpore](https://arxiv.org/abs/2206.12240) - MSAs for 570K PDBs + 745K Distillation

### Databases of predictions
  - AlphaFold Database (UniRef90 | AF2)
    - Manuscript: https://doi.org/10.1093/nar/gkab1061
    - Resource: https://alphafold.ebi.ac.uk
  - Eukaryotic interactormes (Protein-Protein interactions | RF/AF2)
    - Manuscript: https://www.science.org/doi/10.1126/science.abm4805
    - Resource: https://www.ebi.ac.uk/pdbe/news/predicted-complexes-modelarchive-now-pdbe-kb-pages
  - Structures of human-transcriptome isoforms (ColabFold/AF2)
    - Manuscript: https://doi.org/10.1101/2022.06.08.495354
    - Resource: https://www.isoform.io
  - AlphaFill - enriching the AlphaFold models with ligands and co-factors (AF2)
    - Manuscript: https://www.biorxiv.org/content/10.1101/2021.11.26.470110v1
    - Resource: https://alphafill.eu/
  - IgFold Database (OAS | IgFold) - predictions specific to antibody sequences
    - Manuscript: https://www.biorxiv.org/content/10.1101/2022.04.20.488972v2
    - Resource: https://data.graylab.jhu.edu/igfold_oas_paired95.tar.gz

----

<a name="Webservers"></a>
### Webservers
  - Lambda PredictProtein (ColabFold|limit:500AA)
    - Manuscript: https://doi.org/10.1101/2022.08.04.502750
    - Resource: http://embed.predictprotein.org/
  - Robetta (RoseTTAFold)
    - Resource: https://robetta.bakerlab.org/
  - 💀 Moonbear
    - Resource: https://www.getmoonbear.com/
    - Other: [[tweet] Stephanie's announcement](https://twitter.com/stephanieszhang/status/1427773598199164937)
