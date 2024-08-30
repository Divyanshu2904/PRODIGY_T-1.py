# PRODIGY_T-1.py
alphabet=['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z']

def encryption(plain_text,shift_key): 
    cipher_text=""
    for char in plain_text:                            
            position=alphabet.index (char)
            new_position=(position+shift_key)%26
            cipher_text +=alphabet[new_position]
    print(f"Here's is the text after encrytion: {cipher_text}")   

def decryption(cipher_text,shift_key):
    plain_text=""
    for char in cipher_text: 
            position=alphabet.index(char)
            new_position=(position-shift_key)%26
            plain_text +=alphabet[new_position]
    print(f"Here's is the text after decryption: {plain_text}") 

wanna_end=False
while not wanna_end:
    what_to_do=input("type 'encrypt' for encryption,type 'decrypt' for decryption:\n")
    text=input("type your message:\n").lower()
    shift=int(input("enter shift key:\n"))
    if what_to_do=="encrypt":
        encryption(plain_text=text,shift_key=shift)
    elif what_to_do=="decrypt":
        decryption(cipher_text=text,shift_key=shift)
    play_again=input("type 'y' to continue, type 'n' to exit.\n")
    if play_again=='n':
        wanna_end=True
        print("Have a nice day! Bye..")
