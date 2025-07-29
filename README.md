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

## Catatan
- Alamat memmori (DevAddress) menggunakan alamat sesuai hasil scan i2c
- contoh DevAddress AT24Cxx = 0xA0, hasil scan = 0x50; pakai DevAddress 0x50
- data yang disimpam pada EEPROM mengunakan format ASCII
- nilai ASCII harus dikonversi, char to integer

## Referensi
- [**Scan i2c bus**](https://stm32world.com/wiki/STM32_Scan_I%C2%B2C_bus)
- [**i2c Scanner**](https://deepbluembedded.com/stm32-i2c-scanner-hal-code-example/)
- [**Using I2C for any device on STM32 with HAL**](https://youtu.be/cvmQNTVJrzs?si=vujmO-f-T9e0ivx8)
