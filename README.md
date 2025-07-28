# stm32_eeprom
STM32 akses EEPROM AT24C64

## Konfigurasi pin i2c
Gunakan pin I2C PB8 dan PB9 untuk memori

## Konversi Char to Integer data
subtracting the ASCII value of '0'.
- char myChar = '5';
- int myInt = myChar - '0'; // myInt will be 5

Converting a Character Array (String) to an Integer
- #include <stdlib.h> // Required for atoi()
- char myString[] = "123";
- int myInt = atoi(myString); // myInt will be 123

Type Casting (for ASCII Value):
- char myChar = 'A'; // ASCII value of 'A' is 65
- int myInt = (int)myChar; // myInt will be 65

Considerations in STM32CubeIDE:
- Include necessary headers: Ensure you include stdlib.h when using atoi().
- Memory Management: Be mindful of memory allocation when handling character arrays, especially if they are dynamically sized or received via peripherals like UART.
- Error Handling: For atoi(), consider adding error handling if the input string might not be a valid number. You can use strtol() for more robust conversion with error checking.
