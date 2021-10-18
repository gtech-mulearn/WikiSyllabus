# File Handling in C

Many real-life problems involve large volumes of data and in such situations, the console oriented I/O operations pose two major problems.
It becomes cumbersome and time consuming to handle large volumes of data through terminals.
The entire data is lost when either the program is terminated or the computer is turned-off.
It is therefore necessary to have a more flexible approach where data can be stored on the disk and read whenever necessary, 
without destroying the data. This method employs the concept of files to store data.

### File handling functions


| Function name | Operation |
| :----- | :-----|
| fopen( ) | Creates a new file for use / Opens an existing file.|
| fclose( ) | Closes a file which has been open for use. |
| getc( ) | Reads a character from a file. |
| putc( ) | Writes a character to a file. |
| fprintf( ) | Writes a set of data values to a file. |
| fscanf( ) | Reads a set of values from a file. |
| getw( ) | Reads a integer from a file. |
| putw( ) | Writes a integer to a file. |
| fseek( ) | Sets the position to the desired point in file. |
| ftell( ) | Gives the current position in the file. |
| rewind( ) | Sets the position to beginning of file. |