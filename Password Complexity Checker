import re

def check_password_strength(password):
    # criteria for a strong password
    length_criteria = len(password) >= 8
    uppercase_criteria = re.search(r'[A-Z]', password) is not None #checking for "UPPER" case
    lowercase_criteria = re.search(r'[a-z]', password) is not None #checking for "lower" case
    digit_criteria = re.search(r'\d', password) is not None #to check the "digit" availibility
    special_char_criteria = re.search(r'[!@#$%^&*(),.?":{}|<>]', password) is not None #to check special case 

    # checking if the criteria is met
    if all([length_criteria, uppercase_criteria, lowercase_criteria, digit_criteria, special_char_criteria]):
        return "Strong password"
    elif any([length_criteria, uppercase_criteria, lowercase_criteria, digit_criteria, special_char_criteria]):
        return "Moderate password"
    else:
        return "Weak password"

if __name__ == "__main__":
    while True:
        password = input("Enter a password to check its strength: ")
        
        # minimum length requirement
        if len(password) < 8:
            print("The password must be at least 8 characters long. Please try again.")
            continue  # if the minimum length is not met then asking for another password
        
        strength = check_password_strength(password)
        print(f"Password strength: {strength}")
        break  # Exit the loop if a valid password is entered
