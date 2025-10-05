def process_file(input_filename, output_filename):
    """
    Reads the input file, converts its content to uppercase, counts words,
    and writes the processed text and word count to the output file.
    """
    try:
        with open(input_filename, "r") as infile:
            content = infile.read()
        word_count = len(content.split())
        uppercase_content = content.upper() 

        with open(output_filename, "w") as outfile:
            outfile.write("Processed Text:\n")
            outfile.write(uppercase_content + "\n\n")
            outfile.write(f"Word Count: {word_count}\n")
    except Exception as e:
        print(f"An error occurred: {e}")
        return

if __name__ == "__main__":
    input_file = input("Enter the name of the input file (e.g., input.txt): ")
    output_file = "output.txt" # You can also prompt the user if needed

    process_file(input_file, output_file)
