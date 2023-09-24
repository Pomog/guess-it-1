# guess-it

## Usage

You will first need copy the `student/` folder (provided by the student) in which you will see the student guessing program along with a file called `script.sh`. This file should be an executable shell script that runs the student program if you are in the root folder `guess-it/`. The filesystem should look somethings like this:

```console
─ guess-it/
├── ai/
│   ├── big-range
│   └── ...
├── index.html
├── index.js
└── ...
└── student/
    ├── ...
    └── script.sh

```

## Description
The data received by the program, as always, will be presented as the following example:
```bash
189
113
121
114
145
110
...
```
This data represents a graph in which the values of the x axis are the number of the lines (0, 1, 2, 3, 4, 5 ...) and the values of the y axis are the actual numbers (189, 113, 121, 114, 145, 110...).

Each of the numbers will be your standard input and the purpose of your program is for you to find the range in which the next number will be in. This range should have a space separating the lower limit from the upper one like in the example:
```bash
>$ ./your_program
189 --> the standard input
120 200    --> the range for the next input, in this case for the number 113
113 --> the standard input
160 230    --> the range for the next input, in this case for the number 121
121 --> the standard input
110 140    --> the range for the next input, in this case for the number 114
114 --> the standard input
100 200    --> the range for the next input, in this case for the number 145
145 --> the standard input
1 99      --> the range for the next input, in this case for the number 110
110 --> the standard input
100 150    --> the range for the next input, in this case for the number
145
...
```

### Audit checkpoints can be found [here](https://github.com/01-edu/public/tree/master/subjects/guess-it-1/audit)


# In order to test the student program, these commands should be ran to have the dependencies needed and to start the webpage on the port 3000:

npm (Node Package Manager) 

        ```console
        npm install
        node server.js
        ```

or
```console
sudo apt install npm
sudo apt-get update
sudo apt install nodejs
sudo apt install npm
```

check
```console
node -v
npm -v
```

Navigate to the directory where your server.js script is located and open a terminal there. Then, run the following command to install the required dependencies (Express.js):
check
```console
npm install express
```
# The user running the Node.js server should have permission to execute the ./student/script.sh script. 

```console
chmod +x student/script.sh
```

You will need to run also this command inside the `ai/` directory to make the programs executable:

```console
chmod +x *
```

# Run the Server:

```console
node server.js
```




After opening your browser of preference in the port [3000](http://localhost:3000/), if you try clicking on any of the `Test Data` buttons, you will notice that in the Dev Tool/ Console there is a message which tells you that you need another guesser besides the student.

Adding a guesser is simple. You just need to add in the URL a guesser, in other words, the name of one of the files present in the `ai/` folder:

```console
?guesser=<name_of_guesser>
```

For example:

```console
?guesser=big-range
```

### EXAMPLE http://localhost:3000/?guesser=big-range

After that, choose which of the random data set to test. After that you can wait for the program to test all of the values (boooooring), or you can click `Quick` in order to skip the waiting and be presented with the results.

Since the website uses big data sets, we advise you to clear the displays clicking on the `Clean` button after each test.
