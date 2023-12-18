# File Integrity Monitoring Project

## Overview

The File Integrity Monitoring Project enhances security by detecting changes in files, ensuring the integrity of critical data. It provides a PowerShell script for collecting baselines and continuously monitoring files for changes.

## Dependencies

- Powershell
  
## Features

- **Option A: Collect new Baseline**
  - Calculate and store file hashes for future comparisons.
- **Option B: Begin monitoring files with saved Baseline**
  - Continuously monitor files and receive notifications for changes.
 
## Main Script Logic

- User input prompts for action selection (A or B).
- Functions for collecting baseline or monitoring files.
- Continous monitoring loop with notifications.

## Code Structure

### Calculate-File-Hash Function

- Computes the SHA512 hash of a given file path.

```powershell
Function Calculate-File-Hash {
    param($filepath)
    $filehash = Get-FileHash -Path $filepath -Algorithm SHA512
    return $filehash
}
