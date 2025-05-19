import os
import shutil

# Set the path to your Downloads folder (change if needed)
downloads_folder = os.path.expanduser("~/Downloads")

# Define folders for different file types
file_types = {
    'Images': ['.jpg', '.jpeg', '.png', '.gif'],
    'Documents': ['.pdf', '.docx', '.doc', '.txt', '.xlsx', '.pptx'],
    'Videos': ['.mp4', '.mkv', '.mov'],
    'Music': ['.mp3', '.wav'],
    'Archives': ['.zip', '.rar', '.tar', '.gz'],
    'Scripts': ['.py', '.js', '.html', '.css'],
}

def organize_folder():
    for filename in os.listdir(downloads_folder):
        file_path = os.path.join(downloads_folder, filename)

        if os.path.isfile(file_path):
            file_ext = os.path.splitext(filename)[1].lower()

            for folder_name, extensions in file_types.items():
                if file_ext in extensions:
                    target_folder = os.path.join(downloads_folder, folder_name)
                    os.makedirs(target_folder, exist_ok=True)
                    shutil.move(file_path, os.path.join(target_folder, filename))
                    print(f"Moved {filename} to {folder_name}")
                    break

if __name__ == "__main__":
    organize_folder()
    print("Download folder organized!")
