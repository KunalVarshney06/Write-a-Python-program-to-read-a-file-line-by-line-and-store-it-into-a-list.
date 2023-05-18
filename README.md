# Write-a-Python-program-to-read-a-file-line-by-line-and-store-it-into-a-list.
def read_file_into_list(file_path):
    lines = []
    try:
        with open(file_path, 'r') as file:
            lines = file.readlines()
            lines = [line.strip() for line in lines]
    except FileNotFoundError:
        print("File not found.")
    except IOError:
        print("An error occurred while reading the file.")
    return lines

# Example usage
file_path = 'path/to/your/text/file.txt'  # Replace with the actual file path
lines_list = read_file_into_list(file_path)
print("Lines in the file:")
for line in lines_list:
    print(line)
