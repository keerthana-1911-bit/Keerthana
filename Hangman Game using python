import random

word_list = ["python", "hangman", "developer", "program", "keyboard"]
word = random.choice(word_list)

display = ['_'] * len(word)
guessed_letters = []
lives = 6

print("Welcome to Hangman!")

while lives > 0 and '_' in display:
    print("\nCurrent word:", ' '.join(display))
    guess = input("Guess a letter: ").lower()

    if guess in guessed_letters:
        print("You've already guessed that letter.")
        continue

    guessed_letters.append(guess)

    if guess in word:
        for i in range(len(word)):
            if word[i] == guess:
                display[i] = guess
        print("Correct!")
    else:
        lives -= 1
        print(f"Wrong! You have {lives} lives left.")

if '_' not in display:
    print("\nCongratulations! You guessed the word:", word)
else:
    print("\nGame Over! The word was:", word)
