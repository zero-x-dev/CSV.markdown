import pandas as pd

def read_csv_file(file_path):
    try:
        # Read the CSV file into a DataFrame
        df = pd.read_csv(file_path, encoding='utf-8')  # Change encoding if needed
        print(df.to_string(index=False))  
    except FileNotFoundError:
        print(f" File not found: {file_path}")
    except UnicodeDecodeError:
        print(" Unicode decode error: Try using encoding='utf-8-sig' or 'latin1'")
    except Exception as e:
        print(f" An error occurred: {e}")

if __name__ == "__main__":
    csv_path = "C:\\Users\\visha\\Desktop\\stream_of_thoughts.csv" 
    read_csv_file(csv_path)
