🍭 Check if your computer | laptop | PC | machine has typescript installed
Use following command to check
tsc -v
🍭 Initialize ts config
Make folder named typescript-tut inside that folder,
Below command will initialize the tsconfig.json
tsc -init
🍭 Folder structure
Make build folder and inside it make js folder
-build--
   |--Js

Make src folder inside these folder make 01_basics.ts file
From src compiler look for .ts file and compile it into .js file inside build/js folder
-build--
   |--Js

-src--
    |--01_basics.ts
🍭 Changes in tsconfig.json
Go into tsconfig.json and press
ctrl + f
Type rootdir and uncomment that and do following
By doing following action we are telling compiler to look for .ts typescript file inside ./src folder such that it will get compiled into the .js file inside build/js folder
    //"rootDir": "./src", change this into following
    "rootDir": "./src",

Type outdir and uncomment that and do following
By doing following action we are setting compiler to put compiled .js file inside build/js folder
    // "outDir": "./",  change this into following
    "outDir": "./build/js",
Type target and do following change
"target": "es2016",
"target": "ES2022",
🍭 How to compile .ts into .js
Then run following command inside terminal to start compilation of ts files inside ./src into js file inside ./build/js folder this will keep on compilation process whenever you change the file and click ctrl + s
tsc -w
🍭 Nodemon setup to run javascript file inside terminal
If you don't have nodemon installed enter following command to install nodemon
npm install nodemon
Now use ctrl + shift + p to open command pallette and type reload window to reload the vs-code

Now navigate to compiled javascript file which you want ot run inside terminal to get output eg,

cd ./build/js
Run the following command
nodemon ./01_basic.js
So what nodemon will do it whenever you make changes in 01_basic.js the ts compiler compile it into 01_basic.js and then nodemon identify the changes and run the 01_basic.js to give us output
------------>>>>>>>That's it Happy Coding :) <<<<<<<<-----------
