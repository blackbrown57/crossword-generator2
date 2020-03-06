# crossword-generator2
Crossword generator to create web based crosswords. Primarily for CTF uses. The crossword is embedded into an interactive web page. It requires only a "dumb" web server to serve the page. 

Generates crosswords and exports them to a javascript grid and html clues. Requires Python 3.

# Thanks
to Daniel Nögel for the code this was based on.
See https://github.com/dnoegel/crossword-generator for his code.

to the people at Squarectf (https://squarectf.com) for the javascript this is based on.


# License
GPLv3

# To use this code and create an online crossword
1. Create a text file with the questions and answers for the crossword. See questions.txt for a sample
2. Run the generater with the text file as input. Here is an example command line:
  python3 crosswordGenerator.py  --print-js-html-clues --print-js-grid --print-solved-js-grid --stats questions.txt
3. Manually edit the crossword.js file, placing the grid output with answers at the beginning of the file
4. Edit the crossword.html file, placing the HTML clues into the division at the bottom of the page. There is an HTML comment with the words "Place the clues here" at the proper place.
Place the editted crossword.html, crossword.js and md5.js files on your website.
5. Load the file into your browser. Visually verify the crossword and clues are correct.
6. Open the javascript console.
7. Change one of the letters at the end of a word, and change it back to verify the md5 calculation is working. When the values are changed back to all be correct, write down the 6 characters displayed on the console.
8. Edit crossword.js, again, replace the alue of the variable "answerPrefix" with the six characters.
9. Reload the page with the altered crossword.js Verify if you change a character at the end of a word and then change it back, that you get a "You Win!!" message.
10. Edit crossword.js again, and replace the grid with the answers with the grid without the answers.
11. Reload the page and do final testing.

Note: The fine print at the bottom of the generated HTML has a link to a pdf version of the empty crossword. You can either eliminate that text, or create your own pdf.
