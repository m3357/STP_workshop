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

`conda create -n STP_workshop python=3.13.3`
`conda activate STP_workshop
`conda install jupyter`

🍎 macOS
Install Miniconda:

`curl -O https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh`
`bash Miniconda3-latest-MacOSX-arm64.sh`

Create and activate environment:

`conda create -n bioenv python=3.13.3`
`conda activate bioenv`
`conda install jupyter`

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
`conda activate STP_workshop`
`conda create -c bioconda -c conda-forge \ bwa samtools fastqc gatk4`

⚠️ On Apple Silicon (M1/M2), use Rosetta or ensure dependencies match osx-arm64.

🪟 Installation on Windows
✅ Option 1: Using Conda 

`conda activate STP_workshop`
`conda -c bioconda -c conda-forge \ bwa samtools fastqc gatk4`

✅ Option 2: Using Windows Subsystem for Linux (WSL)
Install WSL2 + Ubuntu, then:

`sudo apt update`
`sudo apt install bwa samtools fastqc`

For GATK:
`sudo apt install default-jdk`
`wget https://github.com/broadinstitute/gatk/releases/download/4.5.0.0/gatk-4.5.0.0.zip`
`unzip gatk-4.5.0.0.zip`
`cd gatk-4.5.0.0`
`./gatk --help`
