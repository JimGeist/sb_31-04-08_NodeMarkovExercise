# sb_31-04-08_NodeMarkovExercise

## Assignment Details
## Step 1: 
Creation of code to implement the `makeChains()` and `makeText()` methods of the textural Markov chain generator. Test cases were created to verify the word chains created, the random number generation, and a 2-word make test.

## Step 2: 
involved building the `makeText.js` that will either read text for the generator from a text file for a url.

**Enhancements**

- makeTest.js has a 'main function' and the logic in the main block was kept to a minimum.
- Help is displayed when `makeTest.js` is issued without arguments.
- Error messages added if the file was empty or the web page returned no text.
The enhancements were carried forward from the [step3.js](https://github.com/JimGeist/sb_31-03-13_NodeIntroExercises/commit/f58e9e3cfeac82349b05fec641dd69bd385652c2#diff-17e8dd57193da404fad87a3ccded474d0fe759ad9497d9364898e64f6d2b776b) from the previous exercise.


**Difficulties**
- `await` was not working as expected in the textFromUrl function. The `await` within the function worked but logic in main continued with an unfilled promise. 'async' was added to 'main' and `await` was placed before the call to the textFromUrl function. I am not sure why the logic continued when the axios.get call had an `await`. 
- Overdoing things -- On output, wouldn't it be nice to have the first word capitalized and then have a . after the last word? And it all needed to come out because it was affecting 
testing -- especially capitalizing the first word.
