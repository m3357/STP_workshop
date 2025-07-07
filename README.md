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

1. `conda create -n STP_workshop python=3.13.3`
2. `conda activate STP_workshop`
3. `conda install jupyter`

🍎 macOS
Install Miniconda:

1. `curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh`
2. `bash Miniconda3-latest-MacOSX-arm64.sh`

Create and activate environment:

1. `conda create -n bioenv python=3.13.3`
2. `conda activate bioenv`
3. `conda install jupyter`

💻 Installation on macOS
✅ option1 : Using Homebrew 
Install Homebrew first:

`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`

Then install the tools:

`brew install bwa samtools fastqc`

🔧 For GATK, Homebrew doesn’t support it directly. Use:

1. `brew install openjdk`
2. `wget https://github.com/broadinstitute/gatk/releases/download/4.5.0.0/gatk-4.5.0.0.zip`
3. `unzip gatk-4.5.0.0.zip`
4. `cd gatk-4.5.0.0`
5. `./gatk --help`

✅ Option 2: Using Conda (Cross-platform)
1. `conda activate STP_workshop`
2. `conda create -c bioconda -c conda-forge \ bwa samtools fastqc gatk4`

⚠️ On Apple Silicon (M1/M2), use Rosetta or ensure dependencies match osx-arm64.

🪟 Installation on Windows
✅ Option 1: Using Conda 

1. `conda activate STP_workshop`
2. `conda -c bioconda -c conda-forge \ bwa samtools fastqc gatk4`

✅ Option 2: Using Windows Subsystem for Linux (WSL)
Install WSL2 + Ubuntu, then:

1. `sudo apt update`
2. `sudo apt install bwa samtools fastqc`

For GATK:
1. `sudo apt install default-jdk`
2. `wget https://github.com/broadinstitute/gatk/releases/download/4.5.0.0/gatk-4.5.0.0.zip`
3. `unzip gatk-4.5.0.0.zip`
4. `cd gatk-4.5.0.0`
5. `./gatk --help`
