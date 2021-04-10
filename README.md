<p align="center">
  <a href="" rel="noopener">
 <img width=200px height=200px src="https://www.linkpicture.com/q/chaoss-2.png" alt="Project logo"></a>
</p>

<h3 align="center">CHAOSS Microtasks</h3>

<div align="center">


</div>

---

This repository contains and details all the micro-tasks I executed for [Automate Metrics Release and Process Improvement](https://github.com/chaoss/website/issues/537) Google Summer of Code Project for [CHAOSS](https://www.chaoss.community).



## 📝 Table of Contents

- [About](#about)
- [Microtask 1](#microtask1)
- [Microtask 2](#microtask2)
- [Extra Contribution](#extra)
- [Microtask 3](#microtask3)
- [Getting Started](#getting_started)
- [Prerequisites](#prerequisites)
- [Markdown files](#markdown)
- [Installation](#installation)
- [Creation Process](#creation)
- [Built Using](#built_using)

- [Authors](#authors)
- [Acknowledgments](#acknowledgement)

## 🧐 About <a name = "about"></a>

The official CHAOSS Metrics Release is captured in pdf form at the time of the release by printing each metric page as a PDF and combining them manually. The website pulls in the metrics from Markdown files in the working group GitHub repositories. It would be great if the PDF could be automatically generated from the Markdown files without having to manually PDF print the website pages.
This repository in [Microtask 3](#microtask3) explains how I intend to solve the Metrics Release Automation problem.

## Microtask 1: Attend the weekly community meeting and monthly web content meeting <a name = "microtask1"></a>  

| Date | Meeting name| Status |
| -- | --  | -- |
| March 16, 2021  | CHAOSS Weekly Meeting | Attended |
| March 17, 2021 | Diversity, Equity & Inclusion Meeting | Attended |
| March 23, 2021  | CHAOSS Weekly Meeting | Attended |
| March 24, 2021 | Diversity, Equity & Inclusion Meeting | Attended  |
| March 30, 2021 | CHAOSS Weekly Meeting | Attended |
| March 31, 2021 | Diversity, Equity & Inclusion Meeting | Attended |
| April 6, 2021 | Monthly Web Content Meeting | Attended |

## Microtask 2: Familiar yourself with the website and GitHub repository <a name = "microtask2"></a> 

| Contribution | Status |
| - | - |
| [Update Asia pacific Community README.md](https://github.com/chaoss/website/pull/552) | merged |
| [Create a draft of the Beginners contribution guide](https://github.com/chaoss/website/pull/573) | merged |
| [Update and added extra descriptions to Beginners.md](https://github.com/chaoss/website/pull/578) | merged |
| [Add description for more parts of the website](https://github.com/chaoss/website/pull/593) | merged |
| [Add Intro Workshop to Site](https://github.com/chaoss/website/issues/595) | merged |
| [Make changes to Contributing.md](https://github.com/chaoss/governance/pull/246) | merged | 
| [Add extra description for beginner contributors](https://github.com/chaoss/governance/pull/251) | merged |

### Extra contribution.<a name = "extra"></a> 
I added some documentation to describe the structure of the CHAOSS website deployed from markdown. [Beginners Guide](https://github.com/chaoss/website/tree/master/Beginners%20Guide) takes care of this. This makes navigating the markdown files easier for beginner contributors as they can now logically place where each part of the website is. This is still a work in progress and would continue even if I am accepted as a GSoC participant or not.

## Microtask 3 <a name = "microtask3"></a> 
Create a repository that contains:
* Two (2) markdown files (you can start with files CHAOSS created and modify them as needed).
* A single PDF generated from those markdown files.
* A description of how you generated the PDF from the markdown files.

### 🏁 Getting Started <a name = "getting_started"></a>

This part of this README explains how I generated a single PDF file from 2 markdown files takend from the CHAOSS Project.

### Prerequisites <a name = "prerequisites"></a>
* [Pandoc](https://pandoc.org/)
* [Eisvogel](https://github.com/Wandmalfarbe/pandoc-latex-template)
* [MiKTeX](https://miktex.org/)

Pandoc is a free and open-source document converter, widely used as a writing tool (especially by scholars) and as a basis for publishing workflows.

Eisvogel is a clean pandoc LaTeX template to convert your markdown files to PDF or LaTeX. It is designed for lecture notes and exercises with a focus on computer science. The template is compatible with pandoc 2.

MiKTeX's integrated package manager installs missing components from the Internet, if required. This allows you to keep your TeX installation as minimal as possible (“Just enough TeX”).

### Markdown files<a name = "markdown"></a>
The markdown files were taked from the [release](https://github.com/chaoss/website/tree/master/release) folder on the [CHAOSS Website GitHub Repository](https://github.com/chaoss/website).
The markdown files are listed below:
* [contributors.md](https://github.com/chaoss/website/blob/master/release/contributors.md)
* [release-notes.md](https://github.com/chaoss/website/blob/master/release/release-notes.md)

### Installation<a name = "installation"></a>
Install [Pandoc](https://pandoc.org/) [Eisvogel](https://github.com/Wandmalfarbe/pandoc-latex-template) and [MiKTeX](https://miktex.org/) on your local computer. I currently use Windows as my primary OS so this README details how to successfully create the needed PDF on Windows. 
I decided to use this method of installing Pandoc, Eisvogel and MiKTeX because it is beginner friendly and can easily be used without much technical requirements. 



### Creation Process<a name = "creation"></a>
* I created the [cover page](https://github.com/seun-beta/Microtasks/tree/main/assets) using Canva as a png file. This is less cumbersome compared to using LaTeX. 
* I created a [metadata.yaml](https://github.com/seun-beta/Microtasks/blob/main/metadata.yaml) file. This file contains all the colours and formatting needed to create the PDF. This is easy to manipulate as YAML is in a key value format.
* I then ran the following script on Powershell`:

```
pandoc contributors.md release-notes.md metadata.yaml -o output.pdf --from markdown --template eisvogel --listings
```
The command can be found in [cmd.sh](https://github.com/seun-beta/Microtasks/blob/main/cmd.sh)

I would later change the process using shell scripting which I am currently not very conversant with.

This process creates the [output.pdf file](https://github.com/seun-beta/Microtasks/blob/main/output.pdf)

The output.pdf file has all the necessary listings. Colouring, fonts, hyperlinks and table of contents.


## ⛏️ Built Using <a name = "built_using"></a>

- [Pandoc](https://pandoc.org/) - Document converter
- [Eisvogel](https://github.com/Wandmalfarbe/pandoc-latex-template/releases/latest) - Pandoc LaTeX template
- [MiKTeX](https://miktex.org/) - Minimal TeX package manager
- [Windows Powershell](https://docs.microsoft.com/en-us/powershell/) - Cross Platform automation and configuration management framework 

## ✍️ Authors <a name = "authors"></a>

- [@seun-beta](https://github.com/seun-beta) - Idea & Initial work


## 🎉 Acknowledgements <a name = "acknowledgement"></a>


- References  
https://pandoc.org/  
https://miktex.org/  
https://github.com/Wandmalfarbe/pandoc-latex-template    
https://tex.stackexchange.com/  
