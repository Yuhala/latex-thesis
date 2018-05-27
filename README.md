# Latex Thesis Template for ENSP
This repository contains a thesis latex project template based on the [University of Bristol]( https://github.com/pmem/pmdk) latex template. The project is best suited for ENSP students but anyone can customize it to suit his/her needs.

### Prerequisites
In order to follow the tutorial smoothly, start by installing latex on your machine and any latex editor that suits you; I use [TexStudio]( https://github.com/pmem/pmdk) latex editor. Installing and configuring these is beyond the scope of this tutorial. To use this template with minimal hiccups, you should have a fairly good level of latex knowledge.


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
```
\newglossaryentry{bench}
{
	name = Benchmark,
    description = {In computer science, a benchmark is a test to measure the performance of a system to compare it to others},
    plural = benchmark
}
```
Read the [glossaries documentation](https://www.sharelatex.com/learn/Glossaries) on ShareLatex for more information

## Abstract, titles, dedications
Modifying these is as simple as ABC...change the default lipsum text and enter what you want. Compile each time and view the pdf till you are satisfied with the outcome

## Chapters
Each chapter starts with a small mini table of contents. Modify the corresponding tex file. All figures should be put in the
`figxx` directory for the sake of neatness

#### Troubleshooting
For any strange errors, latex StackExchange forum is your best bet...

## Author

* **Peterson Yuhala** 


## Acknowledgments
[ShareLateX](https://www.sharelatex.com)

* PMDK Source code : https://github.com/pmem/pmdk
