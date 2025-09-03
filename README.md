# EXP : 4 IMPLEMENTATION OFVIGENERE CIPHER

## AIM :
To develop a simple C program to implement Vigenere Cipher.
## DESIGN STEPS :
### Step 1 :
Design of Vigenere Cipher algorithnm
### Step 2 :
Implementation using C or pyhton code
### Step 3 :
1.	The Vigenère cipher uses a series of Caesar ciphers based on letters from a repeating keyword to encrypt text.
2.	A Vigenère square or table is created with 26 rows of the alphabet, each shifted one position left, representing different Caesar cipher shifts.
3.	To encrypt, each letter of the plaintext is matched with a corresponding letter in the keyword, repeated to match the message length.
4.	The letter in the Vigenère table is selected by intersecting the row starting with the keyword letter and the column with the plaintext letter.
5.	The resulting encrypted text is a combination of letters taken from various rows of the Vigenère square, based on the keyword.
6.	Decryption reverses this process by identifying the original plaintext letter from the appropriate row based on the keyword letter.

## PROGRAM :
```
 #include <stdio.h>
 #include <string.h>
 void vigenereCipher(char *text, char *key, int decrypt) {
 int len = strlen(text), keyLen = strlen(key);
 for (int i = 0; i < len; i++) {
 int shift = key[i % keyLen]- 'A';
 text[i] = 'A' + (text[i]- 'A' + (decrypt ? 26- shift : shift)) % 26;
 }
 }
 int main() {
 char text[] = "MYTHILI", key[] = "KEY";
 vigenereCipher(text, key, 0);
 printf("Encrypted Message: %s\n", text);
 vigenereCipher(text, key, 1);
 printf("Decrypted Message: %s\n", text);
 return 0;
 }
```

## OUTPUT :

<img width="1920" height="730" alt="image" src="https://github.com/user-attachments/assets/3b9a89cd-29c4-4159-b996-1193872e5f66" />

## RESULT:
The program implementing the Vigenère cipher for encryption and decryption has been successfully	executed,	and	the	results	have	been	verified.
