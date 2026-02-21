# lcd_hd4478_driver
Lcd HD4478 (and compatible) written in C, tested with xc8 compiler
with small number of change it should work with others microcontrollers


in files lcd_config.h has to be added in project  
#include "lcd_config.h"

in this file configuration is required to be added

LCD_PORT_DATA  - port symbol that is connected to lcd data bus DB0-DB7

typed of connection
LCD_HD4478_8BIT
LCD_HD4478_4BIT - here are required to give to which 4 bits data is connected: 
    LCD_POSITION_4_BIT_HIGH
    LCD_POSITION_4_BIT_LOW


also pins and 
#define LCD_HD4478_RW_USAGE or #define LCD_HD4478_RW_GND (RW connected to gnd, less micro output used)

define LCD_PORT_DATA   PORTC
#define LCD_PORT_TRIS_DATA   TRISC
    
#define LCD_PORT_TRIS_E   TRISBbits
#define LCD_PORT_E         PORTBbits
#define LCD_PORT_E_BIT     B2


#define LCD_PORT_RW        PORTBbits
#define LCD_PORT_RW_BIT     B1
#define LCD_PORT_TRIS_RW   TRISBbits

#define LCD_PORT_RS        PORTBbits
#define LCD_PORT_RS_BIT     B0
#define LCD_PORT_TRIS_RS   TRISBbits


DELAY_MS has to be defined as some function that can be used as a wait\delay function that takes as an argument
required wait time (unsigned int)

