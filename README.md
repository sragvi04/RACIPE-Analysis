# RACIPE-Analysis
This Analysis was a part of a study that explores the inhibitory effects of fasting on Epithelial to Mesenchymal Transition using RACIPE and Genome
Scale Metabolic Modeling during my summer intership programme at IISC. 
The built Gene Regulatory Network (GRN) from literature survey was the basis to create a topology file, which served as input for
RACIPE. RACIPE processed this topology input to generate gene expressions for each stable state of 10,000
models. The gene expression data for six genes—mTOR, AMPK, SNAIL, ZEB, miR-200, and miR-34 which
was subsequently z-normalized. We then determined a score called the metabolic score, calculated as AMPK-mTOR, to capture the fasting state based on gene expressions. A higher expression of AMPK and a
lower expression of mTOR indicated a fasting state, represented by a positive value in the metabolic score.
Similarly, the EMT score was determined by subtracting mesenchymal markers from epithelial markers
(SNAIL + ZEB - miR-200 - miR-34) to predict the direction of the transition epithelial or mesenchymal.
Plots were then generated from this data and were analyzed using the Seaborn library in Python.
