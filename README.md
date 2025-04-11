# anon-ecg
This Bash script removes personally identifiable information (PII) from .xml ECG file by overwriting fields containing PII (e.g. <id>, <birthTime>) with blank values. The original files are preserved in the parent directory and the deidentified files are written to an OUTPUT directory. 

## Dependency
`xmlstarlet`

## Instructions

#### 1. Open Terminal
Press `Command (⌘) + Space` to open **Spotlight Search**. Type **Terminal**, then press `Return ⏎`.
#### 2. Check if `xmlstarlet` is installed
In the terminal window run:
```bash
which xmlstarlet
```
If path is returned (e.g. `/usr/local/bin/xmlstarlet`) then `xmlstarlet` is installed, **skip to step 4**. If it returns nothing (blank line), then `xmlstarlet` is not installed. 
#### 3. Install `xmlstarlet` (optional)
`xmlstarlet` can be installed using [Homebrew](https://brew.sh/) by running: 
```bash
brew install xmlstarlet
```
#### 4. Download and install anon-ecg

## File Organization
Move .xml files into parent directory (e.g. `ECG_files`



## ‼️ Disclaimer ‼️
**THIS SCRIPT IS PROVIDED AS-IS, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED. THE AUTHOR IS NOT RESPONSIBLE FOR ANY DAMAGES OR DATA LOSS RESULTING FROM USE OR MISUSE OF THIS SOFTWARE. THIS SCRIPT IS NOT INTENDED FOR CLINICAL USE. USERS ARE RESPONSIBLE FOR VERIFYING THAT ALL SENSITIVE INFORMATION IS PROPERLY REMOVED BEFORE SHARING DE-IDENTIFIED DATA.**
