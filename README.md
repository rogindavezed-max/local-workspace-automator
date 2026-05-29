# local-workspace-automator
ROGIN SERRANO | IT AUTOMATION PORTFOLIO
import os
from pathlib import Path

def setup_workspace():
    # Identify user's base path dynamically
    base_dir = Path.home() / "Downloads"
    
    active_folder = base_dir / "Project_Active"
    archive_folder = base_dir / "Project_Archive"
    
    # Safely create directories if they don't exist
    for folder in [active_folder, archive_folder]:
        if not folder.exists():
            folder.mkdir(parents=True, exist_ok=True)
            print(f"[SUCCESS] Created directory: {folder}")
        else:
            print(f"[INFO] Directory already exists: {folder}")

if __name__ == "__main__":
    setup_workspace()
