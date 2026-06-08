import hashlib
import sys
import os


target_hash =input("[*] Enter MD5 Hash: ")


password_file = "passwords.txt"


if not os.path.exists(password_file):
    print(f"[!] Error: The file '{password_file}' was not found.")
    print("[*] Please create the file and add some common passwords to test.")
    sys.exit()

print("-" * 50)
print(f"[*] Target MD5 Hash: {target_hash}")
print(f"[*] Loading wordlist from: {password_file}")
print("-" * 50)

try:
    # Open the file containing plain-text passwords
    with open(password_file, "r", encoding="utf-8") as file:
        for line in file:

            plain_password = line.strip()

            if not plain_password:
                continue


            hashed_guess = hashlib.md5(plain_password.encode('utf-8')).hexdigest()


            if hashed_guess == target_hash:
                print("\n[+] SUCCESS! Match Found!")
                print(f"[+] Plain Text Password: {plain_password}")
                print("-" * 50)
                sys.exit()

except KeyboardInterrupt:
    print("\n [!] Process interrupted by the user.")
    sys.exit()

print("\n[-] Password not found in the wordlist.")
print("-" * 50)
