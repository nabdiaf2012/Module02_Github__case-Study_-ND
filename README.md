# Module02_Github__case-Study_-ND
# Nabil Diaf
# File: student_qualifications.py
# Description: This app accepts student last names, first names, and GPAs.
#              It determines whether each student qualifies for the Dean's List
#              (GPA 3.5 or higher) or the Honor Roll (GPA 3.25 or higher).
#              Processing stops when the last name 'ZZZ' is entered.

def main():
    while True:
        # Ask for the student's last name
        last_name = input("Enter student's last name (or 'ZZZ' to quit): ").strip()

        # Quit if the sentinel value is entered
        if last_name.upper() == "ZZZ":
            print("Exiting program. Goodbye!")
            break

        # Ask for the student's first name
        first_name = input("Enter student's first name: ").strip()

        # Ask for the student's GPA as a float
        try:
            gpa = float(input("Enter student's GPA: "))
        except ValueError:
            print("Invalid GPA entered. Please enter a numeric value.\n")
            continue

        # Test for Dean's List (GPA 3.5 or greater)
        if gpa >= 3.5:
            print(f"{first_name} {last_name} has made the Dean's List.")
        # Test for Honor Roll (GPA 3.25 or greater)
        elif gpa >= 3.25:
            print(f"{first_name} {last_name} has made the Honor Roll.")
        else:
            print(f"{first_name} {last_name} does not qualify for the Dean's List or Honor Roll.")

        print()  # Blank line for readability between records


if __name__ == "__main__":
    main()
