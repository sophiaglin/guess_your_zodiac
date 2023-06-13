"""A collection of functions for doing my project."""


def get_personality_traits():
    '''
    Returns a dictionary of personality traits, where each trait is assigned to an number.
   
    '''
    
    traits = {
        1: "Energetic, courageous, confident, and competitive.",
        2: "Patient, reliable, practical, and determined.",
        3: "Versatile, sociable, curious, and adaptable.",
        4: "Sensitive, loyal, intuitive, and nurturing.", 
        5: "Dramatic, confident, generous, and enthusiastic.", 
        6: "Analytical, practical, diligent, and modest.",
        7: "Diplomatic, cooperative, gracious, and fair-minded.",
        8: "Passionate, resourceful, brave, and assertive.",
        9: "Adventurous, optimistic, honest, and intellectual.", 
        10: "Responsible, disciplined, ambitious, and cautious.", 
        11: "Independent, original, humanitarian, and intellectual.", 
        12: "Compassionate, artistic, intuitive, and gentle."
       }
    
    return traits


def get_zodiac_sign(month, day):
    ''' 
    Determines the zodiac sign based on the provided month and day. 
    
    Parameters 
    ----------
    month : integer
        The birth month as an integer. 
    day : integer
        The birth day as an integer. 
        
        
    Returns 
    -------
    str : The corresponding zodiac sign based on the provided month and day. 
    '''
   
    if (month == 1 and day >= 20) or (month == 2 and day <= 18):
        return "Aquarius"
    elif (month == 2 and day >= 19) or (month == 3 and day <= 20):
        return "Pisces"
    elif (month == 3 and day >= 21) or (month == 4 and day <= 19):
        return "Aries"
    elif (month == 4 and day >= 20) or (month == 5 and day <= 20):
        return "Taurus"
    elif (month == 5 and day >= 21) or (month == 6 and day <= 20):
        return "Gemini"
    elif (month == 6 and day >= 21) or (month == 7 and day <= 22):
        return "Cancer"
    elif (month == 7 and day >= 23) or (month == 8 and day <= 22):
        return "Leo"
    elif (month == 8 and day >= 23) or (month == 9 and day <= 22):
        return "Virgo"
    elif (month == 9 and day >= 23) or (month == 10 and day <= 22):
        return "Libra"
    elif (month == 10 and day >= 23) or (month == 11 and day <= 21):
        return "Scorpio"
    elif (month == 11 and day >= 22) or (month == 12 and day <= 21):
        return "Sagittarius"
    else:
        return "Capricorn"
    
    
def guess_zodiac_sign():
    '''
    Guesses the user's zodiac sign based on their selected personality trait. 
    
    Returns 
    -------
    str : If confirmed, it will return'Yay! You guessed correctly based on your selected personality trait!', and if not   confirmed, it will return 'You may try again to see which personality traits match your zodiac sign!'
    '''
    
    confirmed = False  # Variable to track zodiac sign confirmation

    while not confirmed:  # Loop until the zodiac sign is confirmed
        
        print("Welcome! I will try to guess your zodiac sign.\n")
        print("Please answer the following questions:\n")
        print("Please select the personality trait that describes you the most by entering the corresponding number:\n")

        traits = get_personality_traits()
        
        traits_to_signs = {
            # Matching the personality traits to zodiac signs
            "Energetic, courageous, confident, and competitive.": "Aries",
            "Patient, reliable, practical, and determined.": "Taurus",
            "Versatile, sociable, curious, and adaptable.": "Gemini",
            "Sensitive, loyal, intuitive, and nurturing.": "Cancer",
            "Dramatic, confident, generous, and enthusiastic.": "Leo",
            "Analytical, practical, diligent, and modest.": "Virgo",
            "Diplomatic, cooperative, gracious, and fair-minded.": "Libra",
            "Passionate, resourceful, brave, and assertive.": "Scorpio",
            "Adventurous, optimistic, honest, and intellectual.": "Sagittarius",
            "Responsible, disciplined, ambitious, and cautious.": "Capricorn",
            "Independent, original, humanitarian, and intellectual.": "Aquarius",
            "Compassionate, artistic, intuitive, and gentle.": "Pisces"
        }
        # Display the personality traits for the user to choose from
        for number, trait in traits.items():
            print(f"{number}. {trait}")

        while True:
            try:
                
                # Asking the user to enter the corresponding number to their chosen personality trait 
                selected_number = int(input("Enter the number corresponding to your chosen personality trait: "))
                if selected_number not in traits:
                    print("Invalid number. Please try again.")
                else:
                    selected_trait = traits[selected_number]
                    zodiac_sign = traits_to_signs[selected_trait]
                    print("Based on your selected personality trait, I guess your zodiac sign is", zodiac_sign)
                    # Confirm the guessed zodiac sign with the user
                    confirmation = confirm_zodiac_sign(zodiac_sign)

                    if confirmation:
                        return "Yay! You guessed correctly based on your selected personality trait!" # zodiac sign is confirmed
                    else: 
                        break
          
            except ValueError:
                # If the user enters a non-numeric value, display an error
                print("Invalid input. Please enter a number.")
                        
        return "You may try again to see which personality traits match your zodiac sign!"   
        

def get_birthdate(prompt="Enter the month of your birthdate (as a number):\n "):
    '''
    Ask the user to enter their birthdate and validate the input. 
    
    Parameters
    ----------
    prompt : str, optional
        The prompt to display when asking for the birthdate.
        Default value is "Enter the month of your birthdate (as a number):\n ".
    
    Returns
    ------
    tuple[int, int] : A tuple containing the month and day of the birthdate entered by the user. 
    Returns (None, None) if the input is invalid. 
    '''
    
    while True:
        try:
            month = int(input(prompt))
            day = int(input("Enter the day of your birthdate:\n "))
            
            if month < 1 or month > 12 or day < 1 or day > 31:
                print("Invalid date. Please try again.")
                continue 
                
            else:
                return month, day
        
        except ValueError:
            print("Invalid input. Please enter a number.")

                              
def confirm_zodiac_sign(zodiac_sign):
    ''' 
    Confirm the user's zodiac sign based on their birthdate. 
    
    Parameter 
    ---------
    zodiac_sign : str 
        The zodiac sign guessed by the user. 
        
    Returns 
    -------
    bool : True if the user's guessed zodiac sign is confirmed. 
    '''
    
    month, day = get_birthdate()
    sign = get_zodiac_sign(month, day)
    ANSI_BOLD = "\033[1m"
    
    # If the guessed zodiac sign matches the actual zodiac sign, confirm and return True
    if sign == zodiac_sign:
        print("Confirmed! Your zodiac sign is", ANSI_BOLD + zodiac_sign)
        return True
    else:
        # If the guessed zodiac sign is incorrect, display the actual zodiac sign and return False
        print("Oops! It seems like your guessed zodiac sign is not", zodiac_sign)
        print('')
        print("But based on your birthday, your zodiac sign is", ANSI_BOLD + sign)
        return False 
