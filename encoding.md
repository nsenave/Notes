# Some notes about encoding

Not 8-bit clean encodings: Base64, UTF-7

- https://en.wikipedia.org/wiki/Base64
- https://datatracker.ietf.org/doc/html/rfc4648#section-4

> This combination leaves the data unlikely to be modified in transit through information systems, such as email, that were traditionally not 8-bit clean. (cf. https://datatracker.ietf.org/doc/html/rfc4648)
> For example, MIME's Base64 implementation uses A–Z, a–z, and 0–9 for the first 62 values. Other variations share this property but differ in the symbols chosen for the last two values; an example is UTF-7. 

https://en.wikipedia.org/wiki/UTF-7 TLDR: UTF-7 is deprecated nowadays. (https://www.fileformat.info/info/charset/UTF-7/list.htm?start=34000)

Is ASCII 7 or 8 bits ?
- https://stackoverflow.com/questions/14690159/is-ascii-code-in-matter-of-fact-7-bit-or-8-bit
- https://stackovercoder.fr/programming/14690159/is-ascii-code-7-bit-or-8-bit
- https://unix.stackexchange.com/questions/330746/what-is-ascii-7-bit-character-set-and-ascii-8-bit-character-set

> A fixed-width encoding means what it sounds like: all characters are encoded using the same number of bytes. 
> To be ASCII-compatible, a fixed-with encoding must encode all its characters using only one byte, so it can have no more than 256 characters. 
> The most common such encoding nowadays is Windows-1252, an extension of ISO 8859-1.

https://en.wikipedia.org/wiki/ISO-8859-1
https://en.wikipedia.org/wiki/Windows-1252 : single byte encoding

https://www.rapidtables.org/fr/convert/number/ascii-hex-bin-dec-converter.html

### About files and binary representation

- https://stackoverflow.com/questions/1416689/what-exactly-is-the-textual-representation-of-binary-data
- https://en.wikipedia.org/wiki/Binary_file
- https://en.wikipedia.org/wiki/Text_file

> At a generic level of description, there are two kinds of computer files: text files and binary files. 

Lewis, John (2006). Computer Science Illuminated. Jones and Bartlett. ISBN 0-7637-4149-3.
- https://archive.org/details/computersciencei00nell

https://en.wikipedia.org/wiki/Binary-to-text_encoding

> If a binary file is opened in a text editor, each group of eight bits will typically be translated as a single character, and the user will see a (probably unintelligible) display of textual characters. 
> A **hex editor** or viewer may be used to view file data as a sequence of hexadecimal (or decimal, binary or ASCII character) values for corresponding bytes of a binary file.

### Encoding in a terminal

Which encoding does the terminal use / Which encoding are terminals capable of?

https://unix.stackexchange.com/questions/112216/which-terminal-encodings-are-default-on-linux-and-which-are-most-common

TLDR: Unix (debian, ubuntu, ...) terminal are capable of utf8
