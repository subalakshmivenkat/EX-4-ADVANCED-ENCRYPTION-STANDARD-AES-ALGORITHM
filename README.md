# EX-4-AES ALGORITHM
## Aim:
  To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.
## ALGORITHM: 
  1. AES is based on a design principle known as a substitution–permutation. 
  2. AES does not use a Feistel network like DES, it uses variant of Rijndael. 
  3. It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits. 
  4. AES operates on a 4 × 4 column-major order array of bytes, termed the state
## PROGRAM: 
```
#include <stdio.h>
#include <string.h>
void xor_encrypt_decrypt(char *input, char *output, char key) {
    for (int i = 0; i < strlen(input); i++) {
        output[i] = input[i] ^ key;  }
    output[strlen(input)] = '\0'; }
int main() {
    char text[] = "HelloWorld";  // Input text
    char encrypted[100], decrypted[100];
    char key = 'K'; 
    xor_encrypt_decrypt(text, encrypted, key);
    printf("Encrypted text: %s\n", encrypted);
    xor_encrypt_decrypt(encrypted, decrypted, key);
    printf("Decrypted text: %s\n", decrypted);
    return 0;
}
```
## OUTPUT:
![image](https://github.com/user-attachments/assets/f1a1fae5-bf11-4aa1-b9fb-348ea4509211)
## RESULT: 
Thus the data encryption standard algorithm for AES had been implemented successfully.
