# exercise-3
This TypeScript code takes a person's name, stored in the `PersonName` variable, and then performs three operations on it to display the name in lowercase, uppercase, and titlecase. Let's go through each step:

Step 1: Show the name in lowercase
```typescript
let lowercaseName: string = PersonName.toLowerCase();
console.log(lowercaseName);
```
In this step, the `toLowerCase()` method is used on the `PersonName` variable, which converts all the characters in the name to lowercase. The result is stored in the `lowercaseName` variable, and then it is printed to the console using `console.log()`.

Step 2: Show the name in uppercase
```typescript
let uppercaseName: string = PersonName.toUpperCase();
console.log(uppercaseName);
```
In this step, the `toUpperCase()` method is used on the `PersonName` variable, which converts all the characters in the name to uppercase. The result is stored in the `uppercaseName` variable, and then it is printed to the console using `console.log()`.

Step 3: Show the name in titlecase
```typescript
let words: string[] = PersonName.split(" ");
let titlecaseName: string = "";

for (let i = 0; i < words.length; i++) {
    titlecaseName += words[i].charAt(0).toUpperCase() + words[i].slice(1).toLowerCase() + " ";
}

console.log(titlecaseName);
```
In this step, the name is converted to titlecase. First, the `split()` method is used on the `PersonName` variable with a space (" ") as the delimiter. This splits the name into an array of words, which is stored in the `words` variable.

Next, a loop is used to iterate through each word in the `words` array. Within the loop, the first character of each word is converted to uppercase using `charAt(0).toUpperCase()`. Then, the rest of the characters in the word are converted to lowercase using `slice(1).toLowerCase()`. The resulting titlecase word is concatenated with the `titlecaseName` variable, and a space is added to separate each word.

Finally, the `titlecaseName` variable, containing the titlecase name, is printed to the console using `console.log()`.

Example output:
```
Step 1 (Lowercase): muhammad kamran ali rana
Step 2 (Uppercase): MUHAMMAD KAMRAN ALI RANA
Step 3 (Titlecase): Muhammad Kamran Ali Rana
```
