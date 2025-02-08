# DISA STIG Remediation Tool

## Overview

The DISA STIG Remediation Tool is a PowerShell-based application designed to automate the remediation of DISA STIG (Security Technical Implementation Guide) rules. It provides functionalities for testing, verifying, and applying STIG rules across multiple machines. The tool includes a WPF (Windows Presentation Foundation) GUI for user-friendly interaction, allowing users to select execution modes (Local or Distributed), run in different modes (Test, Run, Verify), and generate compliance reports.

## Features

- **Automated STIG Remediation**: Apply STIG rules to ensure compliance.
- **Multiple Execution Modes**: Local and Distributed execution modes.
- **Different Operation Modes**: Test, Run, and Verify modes.
- **Compliance Reporting**: Generate detailed compliance reports in CSV and PDF formats.
- **User-Friendly GUI**: WPF-based interface for easy interaction.
- **Logging**: Detailed logging of all operations for auditing purposes.

## Prerequisites

- PowerShell 5.1 or later
- Administrator privileges for applying changes in Run Mode

## Installation

1. Clone or download the repository to your local machine.
2. Ensure all required modules are located in the `Modules` directory.
3. Ensure the `Data` directory exists for storing STIG files.

## Usage

### Running the Tool

1. Open PowerShell with Administrator privileges (required only for 'Run' Mode).
2. Navigate to the directory containing the `stigscript.ps1` file.
3. Execute the script:
   ```powershell
   .\stigscript.ps1
   ```

### GUI Options

- **Execution Mode**: Select between Local and Distributed execution.
- **Operation Mode**: Choose between Test, Run, and Verify modes.
- **Advanced Options**: Enable to select specific STIG rules for processing.
- **Update STIGs**: Download and update the latest STIG files from the GitHub repository.
- **Run**: Execute the selected operation mode.
- **Cancel**: Cancel the operation and close the tool.

### Modes

- **Test Mode**: Simulates changes without applying them. Logs the operations for preview.
- **Run Mode**: Applies changes to the machine(s). Requires acknowledgment of risks.
- **Verify Mode**: Verifies compliance without making changes. Generates a compliance report.

## Logs and Reports

- Logs are stored in the `Logs` directory under the script's location.
- Compliance reports are generated in CSV format for verification and auditing.

## Updating STIG Files

1. Click the **Update STIGs** button in the GUI.
2. Confirm the update prompt.
3. The tool will download the latest STIG files and update the local repository.
