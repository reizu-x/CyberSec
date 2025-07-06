# C++ Notes

* Types of naming convention
    * "file_size" // Snake Case
    * "FileSize" // Pascal Case
    * "fileSize" // Camel Case
    * "iFileSize" // Hungarian Notation
* Fundamental types

| Type        | Bytes | Range             |
| ----------- | ----- | ----------------- |
| short       | 2     | -32,768 to 32,767 |
| int         | 4     | -2B to 2B         |
| long        | 4     | same              |
| long long   | 8     |                   |

| Type        | Bytes | Range               |
| ----------- | ----- | ------------------- |
| float       | 4     | -3.4E38 to 3.4E38   |
| double      | 8     | -1.7E308 to 1.7E308 |
| long double | 8     | -3.4E932 to 1.7E4832|

| Type       | Bytes | Range             |
| ---------- | ----- | ----------------- |
| bool       | 1     | true/false        |
| char       | 1     |                   |

* double price = 99.99;
* float interestRate = 3.677f;
    * f is a must at the end when typing a float else it will be treated as double.
* long fileSize = 90000L;
    * L is a must at the end when typing long
* char letter = 'a';
    * letters
* bool isValid = false;
    * true/false
* auto
    * auto detects what type is the value.
* {} - Brace initializer
* Number Systems

| System                | Digits       | Example |
| --------------------- | ------------ | ------- |
| Decimal (Base 10)     | 0 - 9        | 255     |
| Binary (Base 2)       | 1,0          | 111111  |
| Hexadecimal (Base 16) | 0 - 9, A - F | 0xFF    |
