# Latex Thesis Template for ENSP
This repository contains a thesis latex project template based on the [University of Bristol]( https://github.com/pmem/pmdk) latex template. The project is best suited for ENSP students but anyone can customize it to suit his/her needs.

### Prerequisites
In order to follow the tutorial smoothly, start by installing latex on your machine and any latex editor that suits you; I use T[TexStudio]( https://github.com/pmem/pmdk) latex editor. Installing and configuring these is beyond the scope of this tutorial. To use this template with minimal hiccups, you should have a fairly good level of latex knowledge.


## Downloading the project to your machine 
To get this starter template on your local machine, you can either download the zip file or clone the project using git

```
git clone https://github.com/Yuhala/latex-thesis.git

```
#### Quick intro
As a quick intro, the project contains 3 main folder: `chapters`, `frontmatter`, and `logos`. The names are pretty self explanatory. Each chapter folder has a figure folder, where all images for the chapter should be put. The `ornaments.pdf` file contains the full documentation for the `latex ornament package` which is used for all the beautiful designs

#### Quick test
In order to do a quick test of the project, open the folder in your latex editor and compile the project. You would probably see some errors but as long as your `memoirthesis.pdf` has reasonable enough content, I think you are good to go.

#### Doing Modifications
Here we would get a little bit into the internals of the project and learn how we can build our project using this as a base

## Frontmatter
The frontmatter consists of the front page, title, gloassaries, abstracts and dedications. For the frontpage corner design, open the `frontmatter/title.tex` file and modify the tikzpicture values. See the ornaments package documentation for more information.

## Glossaries
Glossary items are added in the `memoirthesis.tex` file using the below syntax



#### Troubleshooting
In case you get an `Aborted (core dumped)` error after running the program, simply delete the poolfile and create a new one.




### Compiling and Testing the queue-llist program
#### Quick intro
This program is similar to the one above. It creates two persistent queues q1 and q2 based on linked lists. It then continuously enqueues and dequeues an item from both lists alternatively until the `ctrl-c` signal is sent to the process. The program then tells us whether the item is present in either queues.
#### Compiling 
To compile the queue-llist program cd into the queue-llist directory, assuming your current working directory is `pmdk/src/examples/libpmemobj` . Then run the make file

```
cd queue-llist
make
```
#### Testing
After a successful compilation, the executable file  `fifo` is created. You don't need to manually create the poolfile here; it is created in the program.

The program takes two arguments : the path to a poolfile and the item (use any character). The following command runs the program on a poolfile and 'a' as the content of the node item. If the poolfile exists, the program uses it. Else, it creates a poolfile with the same name. Be careful not to use the same poolfile used in the preceding program.

```
./fifo /dev/shm/poolfile a
```
The program continuously prints statements indicating whether the item has been enqueued or dequeued from either queues.
Hit `ctrl-c` to start the signal handler in the program. The signal handler stops the infinite loop and tells us whether our program is fault resilient or not.

#### Troubleshooting
In case you get an `Aborted (core dumped)` error after running the program, simply delete the poolfile and create a new one.





## Author

* **Peterson Yuhala** 


## Acknowledgments

* PMDK Source code : https://github.com/pmem/pmdk
