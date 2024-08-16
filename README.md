# Rename-file-
import os

# Path to the directory containing the files
path = r"C:\Users\salma\OneDrive\Pictures\Screenshots"
#c:\mywork\linkdln_video\experiment_dl

# Start numbering from 1
i =1

for file_name in os.listdir(path):
    old_file_path = os.path.join(path, file_name)
    
    # Ensure it is a file before renaming
    if os.path.isfile(old_file_path):
        file_extension = os.path.splitext(file_name)[1]
        new_file_name = f'pic{i}{file_extension}'
        new_file_path = os.path.join(path, new_file_name)
        
        # Rename the file
        os.rename(old_file_path, new_file_path)
        print(f"Renamed: {file_name} to {new_file_name}")
        
        i += 1
