# How to get the flag

## First, we need to modify the code in **level3.py**

The code would be like below (in level_3_pw_check() function) :
```
def level_3_pw_check():
    # user_pw = input("Please enter correct password for flag: ")
    # user_pw = input_pw(pos_pw_list)
    for i in pos_pw_list:
        user_pw = i
        user_pw_hash = hash_pw(user_pw)


        if( user_pw_hash == correct_pw_hash ):
            print("Welcome back... your flag, user:")
            decryption = str_xor(flag_enc.decode(), user_pw)
            print(decryption)
            return
        print("That password is incorrect")



```