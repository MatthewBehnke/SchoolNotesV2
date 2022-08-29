#ComputerScience  #IowaStateUniversity  #COMS311 


[[Classes/ISU/COM S 311/COM S 311]] 

---

# Hamming code

Hamming codes find and can correct odd bit errors 

 number each bit left to right starting at 1. Each bit in your data is controlled, plus an extension but for each power of two that you reach in your counting 

Won a [[Turing Award]] in 1968 for this

Hamming won a Turing Award for this 


## Uses
- Able to send self correcting messages
- Error Detection 
- Error detection and correction in hardware memory ECC Memory 

## Online Resources 
- Self correcting messages https://www.youtube.com/watch?v=X8jsijhllIA
- Wikipedia https://en.wikipedia.org/wiki/Hamming_code


## Two bit errors 

The value is nonsense one way to see if it is nonsense is if the value is larger than the total number of bits. 

we need to implement a [[Parity Bit]] onto the hamming code bits. If the parity bit is off then we know that there was a two bit error that was previously undetected using just hamming codes. Now with just one more bit we can do the checking on any input 

If the parity says there is no error and we run the algo and we find an error we know there was a two bit error. Otherwise if the algo says no error then there was no error. Lastly if the parity says there is an error and we run the algo and we find an error then we know that there was only a single bit error and we can correct it. 

If there is a two bit error we can not correct from it. 


## Examples 

### Working
value: 11010111 Hamming code 001110110111

|     | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   | 10  | 11  | 12  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|     | h   | h   | 1   | h   | 2   | 3   | 4   | h   | 5   | 6   | 7   | 8   |
|     | 0   | 0   | 1   | 1   | 1   | 0   | 1   | 1   | 0   | 1   | 1   | 1   |
|     |     |     |     |     |     |     |     |     |     |     |     |     |
| 1   | *   |     | *   |     | *   |     | *   |     | *   |     | *   |     |
| 2   |     | *   | *   |     |     | *   | *   |     |     | *   | *   |     |
| 4   |     |     |     | *   | *   | *   | *   |     |     |     |     | *   |
| 8   |     |     |     |     |     |     |     | *   | *   | *   | *   | *   |


### Error in hamming bit 

value: 0010110

Correct table 

|     | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   | 10  | 11  | 12  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|     | 1   | 0   | 0   | 0   | 0   | 1   | 0   | 1   | 1   | 1   | 0   | 1   |
| 1   | x   |     | x   |     | x   |     | x   |     | x   |     | x   |     |
| 2   |     | x   | x   |     |     | x   | x   |     |     | x   | x   |     |
| 4   |     |     |     | x   | x   | x   | x   |     |     |     |     | x   |
| 8   |     |     |     |     |     |     |     | x   | x   | x   | x   | x   |

Inserted error in hamming code
4 was 0 now 1

|     | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   | 10  | 11  | 12  | correct |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | ------- |
| h   | 1   | 0   | 0   | 1   | 0   | 1   | 0   | 1   | 1   | 1   | 0   | 1   |         | 
| 1   | x   |     | x   |     | x   |     | x   |     | x   |     | x   |     | yes     |
| 2   |     | x   | x   |     |     | x   | x   |     |     | x   | x   |     | yes     |
| 4   |     |     |     | x   | x   | x   | x   |     |     |     |     | x   | no      |
| 8   |     |     |     |     |     |     |     | x   | x   | x   | x   | x   | yes     |


we can see that the fourth row was incorrect which indicates we have an error in our 4 bit which was where our inserted error was.

### 16 bit example 


value: 0110111001010110

|     | 1       | 2       | 3   | 4       | 5   | 6   | 7   | 8       | 9   | 10  | 11  | 12  | 13  | 14  | 15  | 16      | 17  | 18  | 19  | 20  | 21  |
| --- | ------- | ------- | --- | ------- | --- | --- | --- | ------- | --- | --- | --- | --- | --- | --- | --- | ------- | --- | --- | --- | --- | --- |
| h   | ***1*** | ***1*** | 0   | ***0*** | 1   | 1   | 0   | ***0*** | 1   | 1   | 1   | 1   | 0   | 1   | 0   | ***1*** | 1   | 0   | 1   | 1   | 0   |
| 1   | x       |         | x   |         | x   |     | x   |         | x   |     | x   |     | x   |     | x   |         | x   |     | x   |     | x   |
| 2   |         | x       | x   |         |     | x   | x   |         |     | x   | x   |     |     | x   | x   |         |     | x   | x   |     |     |
| 4   |         |         |     | x       | x   | x   | x   |         |     |     |     | x   | x   | x   | x   |         |     |     |     | x   | x   |
| 8   |         |         |     |         |     |     |     | x       | x   | x   | x   | x   | x   | x   | x   |         |     |     |     |     |     |
| 16  |         |         |     |         |     |     |     |         |     |     |     |     |     |     |     | x       | x   | x   | x   | x   | x   |

#### inserting error into bit 21 

|     | 1       | 2       | 3   | 4       | 5   | 6   | 7   | 8       | 9   | 10  | 11  | 12  | 13  | 14  | 15  | 16      | 17  | 18  | 19  | 20  | 21  | correct |
| --- | ------- | ------- | --- | ------- | --- | --- | --- | ------- | --- | --- | --- | --- | --- | --- | --- | ------- | --- | --- | --- | --- | --- | ------- |
| h   | ***1*** | ***1*** | 0   | ***0*** | 1   | 1   | 0   | ***0*** | 1   | 1   | 1   | 1   | 0   | 1   | 0   | ***1*** | 1   | 0   | 1   | 1   | 1   |         |
| 1   | x       |         | x   |         | x   |     | x   |         | x   |     | x   |     | x   |     | x   |         | x   |     | x   |     | x   | no      |
| 2   |         | x       | x   |         |     | x   | x   |         |     | x   | x   |     |     | x   | x   |         |     | x   | x   |     |     | yes     |
| 4   |         |         |     | x       | x   | x   | x   |         |     |     |     | x   | x   | x   | x   |         |     |     |     | x   | x   | no      |
| 8   |         |         |     |         |     |     |     | x       | x   | x   | x   | x   | x   | x   | x   |         |     |     |     |     |     | yes     |
| 16  |         |         |     |         |     |     |     |         |     |     |     |     |     |     |     | x       | x   | x   | x   | x   | x   | no      | 

so 1 + 4 + 16 = 21  or the location of our error 
