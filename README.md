# STP_workshop

I will be adding here all softwares and tools needed for the Module 2 

1. `Genetic Variant analysis`
2. `Comparative Genomics`

💻 Installation on macOS
✅ Using Homebrew 
Install Homebrew first (if not already):

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

Then install the tools:

`brew install bwa samtools fastqc`

🔧 For GATK, Homebrew doesn’t support it directly. Use:

`brew install openjdk
wget https://github.com/broadinstitute/gatk/releases/download/4.5.0.0/gatk-4.5.0.0.zip
unzip gatk-4.5.0.0.zip
cd gatk-4.5.0.0
./gatk --help'
Add to PATH (optional):

bash
Copy
Edit
export PATH="$PATH:$(pwd)"
✅ Option 2: Using Conda (Cross-platform)
bash
Copy
Edit
conda create -n bioenv -c bioconda -c conda-forge \
  bwa samtools fastqc gatk4
conda activate bioenv
⚠️ On Apple Silicon (M1/M2), use Rosetta or ensure dependencies match osx-arm64.

🪟 Installation on Windows
✅ Option 1: Using Conda (Recommended)
Install Miniconda or Anaconda

Then run in Anaconda Prompt:

bash
Copy
Edit
conda create -n bioenv -c bioconda -c conda-forge \
  bwa samtools fastqc gatk4
conda activate bioenv
✅ Option 2: Using Windows Subsystem for Linux (WSL)
Install WSL2 + Ubuntu, then:

bash
Copy
Edit
sudo apt update
sudo apt install bwa samtools fastqc
For GATK:

bash
Copy
Edit
sudo apt install default-jdk
wget https://github.com/broadinstitute/gatk/releases/download/4.5.0.0/gatk-4.5.0.0.zip
unzip gatk-4.5.0.0.zip
cd gatk-4.5.0.0
./gatk --help
