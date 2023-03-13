# Lab Report 5 - Researching More Commands (Week 9)
I will now be choosing the `less` command to research instead of the `find` command 
All were found from this [Link found from google ](https://phoenixnap.com/kb/less-command-in-linux) and Chatgpt
I will be using screenshots instead of codeblock because it is just easier to show somethings this way 
### using `/` while in less command in order to search for a term 
in directory docsearch-main/written_2/travel_guides/berlitz1 
typing `less HandRIbiza.txt` then while in `less` typing `/rating` so that it highlights all instances of this word in this file 

<img width="681" alt="image" src="https://user-images.githubusercontent.com/122490992/224579375-fc0cd6d1-3c97-41c0-831d-80f47dbc160d.png">

With explanation from Chatgpt In summary, the /searchterm command in less allows you to search for a specific string in a file,
and then navigate through the file to find all occurrences of that string. Forwards
now showing this with the `?` command while in `less`
`less HandRIbiza.txt`
which will show the same highlights as such
<img width="681" alt="image" src="https://user-images.githubusercontent.com/122490992/224580706-58393482-150b-4707-afe1-d3adb4c1fc0d.png">

It is essentially the same thing but instead it searches backwards for the specified string.

### using the `-N` command with `less`
Using command `less -N HandRIbiza.txt` as such 

<img width="681" alt="image" src="https://user-images.githubusercontent.com/122490992/224581049-a5db2d2d-f372-41a3-97cb-81fce26ecc20.png">
This will display the line numbers of the file 

getting more specific with the `+` command 
`less -N +10 HandRIbiza.txt`
<img width="681" alt="image" src="https://user-images.githubusercontent.com/122490992/224581154-8da2afbc-da36-4523-9103-5a56f438385d.png">

Showing that displays starting at line 10


### Using the `less` command to open mulitiple files 
In this case using paths 

`less written_2/travel_guides/berlitz1/HandRIbiza.txt written_2/non-fiction/OUP/Castro/chY.txt`

<img width="848" alt="image" src="https://user-images.githubusercontent.com/122490992/224582740-d5db89a4-b308-4bab-8663-c03ec4194e37.png">
In order to go to the next file you have to type `:n` while in less and the second file will be outputed 
<img width="1144" alt="image" src="https://user-images.githubusercontent.com/122490992/224582800-d17fac23-dbbe-4557-a376-ed86ef39ce10.png">

This Open multiple files simultaneously using less without losing the current position in the files. 
To open multiple files, specify file names one after another. As given from the website 
could also just use on text files and not paths 

`less HandRIbiza.txt HandRIsrael.tx`
<img width="1144" alt="image" src="https://user-images.githubusercontent.com/122490992/224583082-77d245f5-2289-4ad7-8b11-52ad5db29752.png">
then  `:n`
<img width="1144" alt="image" src="https://user-images.githubusercontent.com/122490992/224583113-00d0ba1a-d9bb-459c-8d83-8b0113f42f83.png">


### using `-X` command

`less -X  HandRIbiza.txt `

<img width="1144" alt="image" src="https://user-images.githubusercontent.com/122490992/224583237-83d62d54-8fa0-4962-8b45-031ae45ecc18.png">
This will keep the content on the screen after quitting as such 
<img width="1144" alt="image" src="https://user-images.githubusercontent.com/122490992/224583279-ae447c0d-897d-446f-bf75-be0933d6506e.png">

### Using `=` while in `less` 
<img width="1144" alt="image" src="https://user-images.githubusercontent.com/122490992/224583560-9615872e-fb76-479b-b121-e42af89d2d7c.png">
This will show the stats of the file 

Some of these could not be shown in a unique enough way to distinguish themselves from one another so I added the two different things instead with `-X` and `=`.
Again most of this information was found through the link at the top of this page and ChatGPT
