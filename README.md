# Smart-dictionary-and-vocabulary-helper
 Python project that stores 10 English words with their meanings, Urdu, and Spanish translations. The user enters a word, views its meaning, and picks a translation from a simple menu. It handles uppercase and lowercase input and shows a friendly message if the word is not found.
vocabulary = {
    "happy": {
        "meaning"  : "Feeling or showing pleasure or contentment.",
        "urdu"     : "خوش (Khush)",
        "spanish"  : "Feliz"
    },
    "brave": {
        "meaning"  : "Ready to face danger or pain without showing fear.",
        "urdu"     : "بہادر (Bahadur)",
        "spanish"  : "Valiente"
    },
    "knowledge": {
        "meaning"  : "Facts, information, and skills acquired through experience or education.",
        "urdu"     : "علم (Ilm)",
        "spanish"  : "Conocimiento"
    },
    "beautiful": {
        "meaning"  : "Pleasing the senses or mind aesthetically.",
        "urdu"     : "خوبصورت (Khubsoorat)",
        "spanish"  : "Hermoso/a"
    },
    "freedom": {
        "meaning"  : "The power or right to act, speak, or think as one wants.",
        "urdu"     : "آزادی (Azadi)",
        "spanish"  : "Libertad"
    },
    "honest": {
        "meaning"  : "Free of deceit; truthful and sincere.",
        "urdu"     : "ایماندار (Imaandar)",
        "spanish"  : "Honesto/a"
    },
    "patience": {
        "meaning"  : "The ability to accept delay or trouble without getting angry.",
        "urdu"     : "صبر (Sabr)",
        "spanish"  : "Paciencia"
    },
    "dream": {
        "meaning"  : "A cherished aspiration or ambition.",
        "urdu"     : "خواب (Khwaab)",
        "spanish"  : "Sueño"
    },
    "courage": {
        "meaning"  : "The ability to do something that frightens you; bravery.",
        "urdu"     : "ہمت (Himmat)",
        "spanish"  : "Coraje"
    },
    "friend": {
        "meaning"  : "A person with whom you share a bond of mutual affection.",
        "urdu"     : "دوست (Dost)",
        "spanish"  : "Amigo/a"
    }
}
 
# --- STEP 2: Welcome the user ---
print("=" * 50)
print("   Welcome to the Smart Dictionary!")
print("   Meanings + Urdu & Spanish Translations")
print("=" * 50)
 
# --- STEP 3: Ask the user to enter a word ---
# .strip()  removes any accidental spaces around the word
# .lower()  converts the input to lowercase so 'Happy' == 'happy'
user_input = input("\nEnter a word to look up: ").strip().lower()
 
# --- STEP 4: Check if the word exists in our dictionary ---
if user_input in vocabulary:
 
    # Retrieve the nested dictionary for the matched word
    word_data = vocabulary[user_input]
 
    # Display the English meaning right away
    print("\nWord     :", user_input.capitalize())
    print("Meaning  :", word_data["meaning"])
 
    # --- STEP 5: Show a simple translation menu ---
    print("\nWould you like to see a translation?")
    print("  1 - Urdu Translation")
    print("  2 - Spanish Translation")
    print("  3 - Both Translations")
    print("  4 - Exit")
 
    # Ask the user to pick an option
    choice = input("\nEnter your choice (1 / 2 / 3 / 4): ").strip()
 
    # --- STEP 6: Respond based on the user's menu choice ---
    if choice == "1":
        # Show only the Urdu translation
        print("\nUrdu Translation    :", word_data["urdu"])
 
    elif choice == "2":
        # Show only the Spanish translation
        print("\nSpanish Translation :", word_data["spanish"])
 
    elif choice == "3":
        # Show both translations together
        print("\nUrdu Translation    :", word_data["urdu"])
        print("Spanish Translation :", word_data["spanish"])
 
    elif choice == "4":
        # User chose to exit without seeing a translation
        print("\nOkay! Exiting. Happy learning!")
 
    else:
        # Handle any input that isn't 1, 2, 3, or 4
        print("\nInvalid choice. Please run the program again and enter 1, 2, 3, or 4.")
 
else:
    # --- STEP 7: Word not found — show a friendly error ---
    print(f"\nSorry! The word '{user_input}' was not found in the dictionary.")
    print("   Try one of these available words:")
 
    # List all available words so the user knows what to try
    for word in vocabulary:
        print("  -", word.capitalize())
 
# --- STEP 8: Friendly closing message ---
print("\n" + "=" * 50)
print("   Thanks for using the Smart Dictionary!")
print("=" * 50)
 
