# VoiceDNA Evaluation Script

This script is used to evaluate VoiceDNA verification results based on ground truth data and exported voicedna result files.

## Parameters

| Parameter | Description |
|------------|--------------|
| `label_file` | Path to the ground truth file (must follow the provided template format). |
| `score_file` | Path to the exported VoiceDNA result file. |
| `save_report_file` | Path to the output report file (will be generated in the internal test result format). |
| `save_far_tar_file` | Path to the output file containing information about **FAR**, **TAR**, and **threshold**. |
| `auto_calculate_threshold` | Set to `True` to calculate threshold automatically (recommended). Set to `False` to use a predefined threshold. Default: `True`. |

## Usage

1. Edit the file  
   `/Users/fido/scripts/run.sh`  
   and update the parameters above as needed.

   - **Option 1: Auto-calculate threshold (recommended)**  
     ```bash
     auto_calculate_threshold=True
     ```

   - **Option 2: Use predefined threshold**  
     ```bash
     auto_calculate_threshold=False
     ```

   > Note: Both options apply a single threshold for all verification pairs.

2. Open a terminal.

3. Run the following command:
   ```bash
   bash /Users/fido/scripts/run.sh
