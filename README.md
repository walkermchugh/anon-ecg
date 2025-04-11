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
#### 4. Download `anon-ecg.sh` and make executable 
Download the script with `curl`:
```bash
curl -o anon-ecg.sh https://raw.githubusercontent.com/walkermchugh/anon-ecg/main/anon-ecg.sh
```
Then make it executable:
```bash
chmod +x anon-ecg.sh
```
### 5. Run the script
Run the script like this:
```bash
./anon-ecg.sh <input_directory> <output_directory>
```
The script takes two arguments:
1. `<input_directory>` where `input` `.xml' ECG files are located
2. `<output_directory>` where deidentified `output` `.xml` ECG files will be written with a `deid_` prefix
Here is an example:
```bash
./anon-ecg.sh ~/Desktop/ecg_files ~/Desktop/ecg_files/output
```

## File Organization
1. Move .xml files into parent directory, this will be the `<input_directory>`.
2. Create an output director (e.g. `~/Desktop/ecg_files/output`), this will be the `<output_directory>`.


## ‼️ Legal ‼️
**THIS SCRIPT IS PROVIDED AS-IS, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED. THE AUTHOR IS NOT RESPONSIBLE FOR ANY DAMAGES OR DATA LOSS RESULTING FROM USE OR MISUSE OF THIS SOFTWARE. THIS SCRIPT IS NOT INTENDED FOR CLINICAL USE. USERS ARE RESPONSIBLE FOR VERIFYING THAT ALL SENSITIVE INFORMATION IS PROPERLY REMOVED BEFORE SHARING DE-IDENTIFIED DATA.**
