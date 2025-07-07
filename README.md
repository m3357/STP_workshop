# STP_workshop

I will be adding here all softwares and tools needed for the Module 2 

1. `Genetic Variant analysis`
2. `Comparative Genomics`

🪶 Install Miniconda (Lightweight Conda + Python)

🪟 Windows
Download Miniconda:

Miniconda Windows 64-bit (https://www.anaconda.com/docs/getting-started/miniconda/main)

Install:

Run the .exe file → Add to PATH when asked.

Open Anaconda Prompt, then:

`conda create -n bioenv python=3.10
conda activate bioenv
conda install jupyter`
🍎 macOS
Install Miniconda:

bash
Copy
Edit
curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh
bash Miniconda3-latest-MacOSX-arm64.sh
Create and activate environment:

bash
Copy
Edit
conda create -n bioenv python=3.10
conda activate bioenv
conda install jupyter

💻 Installation on macOS
✅ option1 : Using Homebrew 
Install Homebrew first:

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

Then install the tools:

`brew install bwa samtools fastqc`

🔧 For GATK, Homebrew doesn’t support it directly. Use:

`brew install openjdk`
`wget https://github.com/broadinstitute/gatk/releases/download/4.5.0.0/gatk-4.5.0.0.zip`
`unzip gatk-4.5.0.0.zip`
`cd gatk-4.5.0.0`
`./gatk --help`

✅ Option 2: Using Conda (Cross-platform)

`conda create -n bio -c bioconda -c conda-forge \ bwa samtools fastqc gatk4`
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
