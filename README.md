def create_file():
    try:
        with open("my_file.txt", "w") as file:
            file.write("This is line 1\n")
            file.write("12345\n")
            file.write("Another line with some text and numbers: 42\n")
        print("File 'my_file.txt' created successfully with initial content.")
    except PermissionError:
        print("Permission error: Unable to create file.")
    except Exception as e:
        print("An error occurred:", e)
    finally:
        print("File creation process completed.")


def read_and_display():
    try:
        with open("my_file.txt", "r") as file:
            contents = file.read()
            print("\nContents of my_file.txt:")
            print(contents)
    except FileNotFoundError:
        print("File not found: 'my_file.txt' does not exist.")
    except Exception as e:
        print("An error occurred:", e)
    finally:
        print("File reading process completed.")


def append_to_file():
    try:
        with open("my_file.txt", "a") as file:
            file.write("Appending line 1\n")
            file.write("Appending line 2\n")
            file.write("Appending line 3\n")
        print("\nThree lines appended to my_file.txt successfully.")
    except PermissionError:
        print("Permission error: Unable to append to file.")
    except Exception as e:
        print("An error occurred:", e)
    finally:
        print("File appending process completed.")



create_file()
read_and_display()
append_to_file()
