# UpRegScan
UpRegScan 🧬
Upstream Region & Promoter Scanner for Prokaryotic Genomes

Characterize transcriptional frontiers of genes in bacterial genomes

🚀 Overview
UpRegScan is a powerful Python tool designed for the in-depth analysis of upstream regulatory regions in prokaryotic genomes. It helps researchers understand the transcriptional landscape of bacterial genes by:

Calculating Upstream Distances: Determines the precise distances from gene start codons to their nearest upstream genomic boundaries, considering gene orientation and potential overlaps.
Identifying Leaderless Transcripts: Flags potential leaderless mRNA candidates by identifying genes with very short upstream regions (typically less than 10 bp).
Discovering Promoter Motifs: Scans upstream sequences for canonical -10 and -35 promoter box motifs, characteristic of Sigma-A factor-dependent transcription (e.g., in Bacillus subtilis and E. coli).
Visualizing Upstream Length Distributions: Generates informative plots to visualize the distribution of upstream region lengths across different organisms.
Correlating Upstream Lengths with Gene Features: Explores relationships between upstream region lengths, gene lengths, and predicted gene functions (products).
💡 Applications
UpRegScan is a valuable resource for various bioinformatics and microbiology research areas, including:

Transcriptional Unit Architecture Analysis: Gain insights into how genes are organized and regulated at the transcriptional level in bacteria.
Genome Packaging Studies: Identify characteristics indicative of densely packed genomes, where intergenic regions are minimal.
Gene Expression Promoter Identification: Pinpoint potential promoter sequences that could be crucial for gene expression studies or synthetic biology applications.
Leaderless mRNA Research: Facilitate the investigation and identification of genes likely to be translated from leaderless mRNAs, which lack a 5' untranslated region (UTR).
🛠️ Installation
Dependencies
Before you can use UpRegScan, ensure you have the following Python libraries installed. You can install them using pip:

Bash

pip install pandas matplotlib seaborn requests tqdm
Cloning the Repository
To get started, clone the UpRegScan repository to your local machine:

Bash

git clone https://github.com/your-username/UpRegScan.git
cd UpRegScan
(Note: Replace your-username with your actual GitHub username.)

🚀 Usage
(Here, you would typically add detailed instructions on how to run your script, including example commands, what input files are needed, and what output to expect. For instance, you could show how to execute main() from your script.)

Python

# Example of how a user might run the analysis after setting up
# (Assuming your script is named `upregscan_script.py`)
python upregscan_script.py
Customizing Organisms
The ORGANISMS dictionary within the script (upregscan_script.py in the example above) defines the bacterial genomes to be analyzed. You can easily modify this dictionary to include or exclude organisms by updating their NCBI FASTA and GFF URLs.

Python

# Example from your code:
ORGANISMS = {
    "Thermus thermophilus": {
        "fasta_url": "https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/016/865/295/GCF_016865295.1_ASM1686529v1/GCF_016865295.1_ASM1686529v1_genomic.fna.gz",
        "gff_url": "https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/016/865/295/GCF_016865295.1_ASM1686529v1/GCF_016865295.1_ASM1686529v1_genomic.gff.gz"
    },
    # ... more organisms
}
📈 Output
UpRegScan generates both textual statistics and graphical visualizations:

Statistical Report
A detailed statistical report is printed to the console, providing insights into:

Total number of genes analyzed.
Counts and percentages of genes with upstream regions greater than specified thresholds (e.g., 10, 50, 100, 200 bp).
The number and percentage of genes with zero-length upstream regions (indicating overlaps or very tight packing).
The count and percentage of potential leaderless transcripts (upstream &lt; 10 bp).
Average upstream region length.
The number and percentage of genes identified with both -10 and -35 promoter motifs.
A sample of unique gene products found.
Visualizations
The tool generates several plots to visually represent the data, including:

Histogram of Upstream Lengths: Shows the distribution of upstream region lengths for each organism, often with a logarithmic y-axis for better visibility of shorter regions.
Boxplot of Upstream Lengths: Provides a summary of the central tendency and spread of upstream lengths across different organisms.
Violin Plot of Upstream Lengths (Optional): If gene product information is sufficiently extracted, this plot can show the distribution of upstream lengths, potentially grouped by functional categories or organisms.
Scatter Plot: Gene Length vs. Upstream Length: Illustrates any correlation between the length of a gene and the length of its upstream region, using logarithmic scales for both axes.
🤝 Contributing
We welcome contributions to UpRegScan! If you have ideas for new features, bug fixes, or improvements, please feel free to:

Fork the repository.
Create a new branch (git checkout -b feature/YourFeatureName).
Make your changes.
Commit your changes (git commit -m 'Add YourFeatureName').
Push to the branch (git push origin feature/YourFeatureName).
Open a Pull Request.
