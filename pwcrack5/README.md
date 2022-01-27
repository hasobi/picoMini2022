# How to get the flag

1. Edit the level5.py file and add code to read the dictionary.

The code would look like this:
```
pos_pw_list = open('dictionary.txt', 'r')

def level_5_pw_check():
    # user_pw = input("Please enter correct password for flag: ")
    # user_pw_hash = hash_pw(user_pw)
    for i in pos_pw_list:
        user_pw = i.strip()
        user_pw_hash = hash_pw(user_pw)
    
        if( user_pw_hash == correct_pw_hash ):
            print("Welcome back... your flag, user:")
            decryption = str_xor(flag_enc.decode(), user_pw)
            print(decryption)
            return
        print("That password is incorrect")

```