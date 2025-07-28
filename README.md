# Exercise-1---The-Story-of-Caesar-s-Traditional-Secret-Party
#Question 5:
```
let partyLocation = "GARDEN";
const shiftValue = 3;
let encryptedMessage = "";

for (let i = 0; i < partyLocation.length; i++) {
  let char = partyLocation.charCodeAt(i);
  // Check if the character is an uppercase letter (A=65, Z=90)
  if (char >= 65 && char <= 90) {
    char = char + shiftValue;
    // Handle wrapping around Z to A
    if (char > 90) {
      char = char - 26;
    }
  }
  encryptedMessage += String.fromCharCode(char);
}

console.log(encryptedMessage); // Output: JDUGHQ
```
#Question 6:
```
let encryptedMessage = "JDUGHQ";
const shiftValue = 3;
let decryptedMessage = "";

for (let i = 0; i < encryptedMessage.length; i++) {
  let char = encryptedMessage.charCodeAt(i);
  // Check if the character is an uppercase letter (A=65, Z=90)
  if (char >= 65 && char <= 90) {
    char = char - shiftValue;
    // Handle wrapping around A to Z
    if (char < 65) {
      char = char + 26;
    }
  }
  decryptedMessage += String.fromCharCode(char);
}

console.log(decryptedMessage); // Output: GARDEN
```
