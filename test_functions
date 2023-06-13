from my_functions import get_personality_traits, get_zodiac_sign, guess_zodiac_sign, get_birthdate

import mock

import builtins

def test_get_personality_traits(): 
    
    traits = get_personality_traits()
   
    assert all(isinstance(value,str) for value in traits.values())
    assert all(len(value) > 0 for value in traits.values())
    assert len(traits) == 12 
    assert traits[1] == "Energetic, courageous, confident, and competitive."
    assert traits[2] == "Patient, reliable, practical, and determined."
    assert traits[3] == "Versatile, sociable, curious, and adaptable."
    assert traits[4] == "Sensitive, loyal, intuitive, and nurturing."
    assert traits[5] == "Dramatic, confident, generous, and enthusiastic."
    assert traits[6] == "Analytical, practical, diligent, and modest."
    assert traits[7] == "Diplomatic, cooperative, gracious, and fair-minded."
    assert traits[8] == "Passionate, resourceful, brave, and assertive."
    assert traits[9] == "Adventurous, optimistic, honest, and intellectual."
    assert traits[10] == "Responsible, disciplined, ambitious, and cautious."
    assert traits[11] == "Independent, original, humanitarian, and intellectual."
    assert traits[12] == "Compassionate, artistic, intuitive, and gentle."
    

def test_get_zodiac_sign(): 
    
    # Cases with expected results
    assert get_zodiac_sign(1, 25) == "Aquarius"
    assert get_zodiac_sign(2, 19) == "Pisces"
    assert get_zodiac_sign(3, 21) == "Aries"
    assert get_zodiac_sign(4, 20) == "Taurus"
    assert get_zodiac_sign(5, 21) == "Gemini"
    assert get_zodiac_sign(6, 21) == "Cancer"
    assert get_zodiac_sign(7, 23) == "Leo"
    assert get_zodiac_sign(8, 23) == "Virgo"
    assert get_zodiac_sign(9, 23) == "Libra"
    assert get_zodiac_sign(10, 23) == "Scorpio"
    assert get_zodiac_sign(11, 22) == "Sagittarius"
    assert get_zodiac_sign(12, 25) == "Capricorn"
    
    #Additional tests 
    assert get_zodiac_sign(1, 1) == "Capricorn"
    assert get_zodiac_sign(2, 18) == "Aquarius"
    assert get_zodiac_sign(3, 20) == "Pisces"
    assert get_zodiac_sign(4, 19) == "Aries"
    assert get_zodiac_sign(5, 20) == "Taurus"
    assert get_zodiac_sign(6, 20) == "Gemini"
    assert get_zodiac_sign(7, 22) == "Cancer"
    assert get_zodiac_sign(8, 22) == "Leo"
    assert get_zodiac_sign(9, 22) == "Virgo"
    assert get_zodiac_sign(10, 22) == "Libra"
    assert get_zodiac_sign(11, 21) == "Scorpio"
    assert get_zodiac_sign(12, 21) == "Sagittarius"
    
    
def test_guess_zodiac_sign():
    # Test case 1: Test with confirmed zodiac sign
    selected_trait = "Energetic, courageous, confident, and competitive."
    zodiac_sign = "Aries"

    def mock_confirm(sign):
        return sign == zodiac_sign

        assert guess_zodiac_sign(mock_confirm) == "Yay! You guessed correctly based on your selected personality trait!"

    # Test case 2: Test with unconfirmed zodiac sign
    selected_trait = "Energetic, courageous, confident, and competitive."
    zodiac_sign = "Taurus"

    def mock_confirm_zodiac_sign(sign):
        
        return sign == zodiac_sign

        assert guess_zodiac_sign(mock_confirm) == "You may try again to see which personality traits match your zodiac sign!"
        expected = None  # Return value for invalid date
        assert result == expected
        assert result is None
        

def test_get_birthdate():
    with mock.patch('builtins.input', side_effect=['2', '15']):
        assert get_birthdate() == (2, 15)

    with mock.patch('builtins.input', side_effect=['13', '32', '5', '20']):
        assert get_birthdate() == (5, 20)

    with mock.patch('builtins.input', side_effect=['invalid', '7', '25']):
        assert get_birthdate() == (7, 25)

    with mock.patch('builtins.input', side_effect=['11', 'invalid', '3', '10']):
        assert get_birthdate() == (3, 10)
