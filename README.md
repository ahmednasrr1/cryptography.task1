import string

def caesar_brute_force(ciphertext):
    alphabet = string.ascii_uppercase 
    ciphertext = ciphertext.upper()


    for shift in range(1, 26): 
        decrypted_text = ""
        for char in ciphertext:
            if char in alphabet:
                original_index = (alphabet.index(char) - shift) % 26
                decrypted_text += alphabet[original_index]
            else:
                decrypted_text += char  

        print(f"Shift {shift}: {decrypted_text}")



ciphertext = input("Enter the encrypted message: ")
print("\nAttempting to decrypt using brute force:\n")
caesar_brute_force(ciphertext)
