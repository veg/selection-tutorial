# Selection analyses in HyPhy

Presentation notes (in the `assets` folder) and example files in the `data` folder for how to perform selection analyses in [HyPhy](https://hyphy.org)

For additional analyses, you will need the [hyphy-analyses](https://github.com/veg/hyphy-analyses) repository. Via `git clone https://github.com/veg/hyphy-analyses.git`

View the presentation (2023) at https://veg.github.io/selection-tutorial

## Installation

Via Anaconda `conda install -c bioconda hyphy`

To compile from source follow the instructions at http://hyphy.org/download

## Example commands

### FitMG94
`hyphy hyphy-analyses/FitMG94/FitMG94.bf --alignment data/WestNileVirus_NS3.fna --output results/WestNileVirus_NS3.fna.FITTER.json --lrt Yes`


### BUSTED
`hyphy busted --srv No --alignment data/HIV-sets.nex --starting-points 5 --output results/HIV-sets.nex.BUSTED.json`

`hyphy busted --srv No --alignment data/WestNileVirus_NS3.fna --starting-points 5 --output results/WestNileVirus_NS3.fna.BUSTED.json`

`hyphy busted --srv No --alignment data/spike.fas --tree data/spike.tree --starting-points 5 --output results/spike.fas.BUSTED.json`

### aBSREL

`hyphy absrel --alignment data/HIV-sets.nex --output results/HIV-sets.nex.aBSREL.json`

`hyphy absrel --alignment data/WestNileVirus_NS3.fna --output results/WestNileVirus_NS3.fna.aBSREL.json`

`hyphy absrel --alignment data/spike.fas --tree data/spike.tree --branches Internal --output results/spike.fas.aBSREL.json`

### MEME

`hyphy meme --alignment data/HIV-sets.nex --output results/HIV-sets.nex.MEME.json`

`hyphy meme --alignment data/spike.fas --tree data/spike.tree --output results/spike.fas.MEME.json`

`hyphy meme --alignment data/spike.fas --tree data/spike.tree --output results/spike.fas.MEME-Internal.json --branches Internal`

### FEL

`hyphy fel --alignment data/spike.fas --tree data/spike.tree --branches Internal --output results/spike.fas.FEL-Internal.json`

`hyphy fel --alignment data/spike.fas --tree data/spike.tree --branches Internal --output results/spike.fas.FEL-Internal-PBS.json --resample 100`

`hyphy fel --alignment data/WestNileVirus_NS3.fna --ci Yes --output results/WestNileVirus_NS3.fna.FEL-ci.json`

### SLAC

`hyphy slac --alignment data/spike.fas --tree data/spike.tree --branches Internal --output results/spike.fas.SLAC.json`

### RELAX

`hyphy relax --alignment data/AlphaDeltaSpike.fas --tree data/AlphaDeltaSpike.tree --test Delta --reference Alpha  --starting-points 5 --output results/AlphaDeltaSpike.fas.RELAX.json`

### Contrast-FEL

`hyphy contrast-fel --alignment data/AlphaDeltaSpike.fas --tree data/AlphaDeltaSpike.tree --branch-set Alpha --branch-set Delta --output results/AlphaDeltaSpike.fas.CFEL.json`

### GARD, FMM, BSMH
