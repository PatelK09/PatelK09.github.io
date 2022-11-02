# Hosting a resume on GitHub pages

## Table of Contents
* [Purpose](#purpose)
* [Prerequisites](#prerequisites)
* [Instructions](#instructions)
* [More Recources](#more-recources)
* [Authors and Acknowledgments](#authors-and-acknowledgments)
* [FAQs](#faqs)

## Purpose

This README describes the practical steps from Andrew Etter's book Modern Technical Writing on how to host and format a resuming using the [Markdown](https://www.markdownguide.org/), [Markdown editor](https://code.visualstudio.com/docs/languages/markdown), [GitHub pages](https://pages.github.com/), and [Jekyll](https://jekyllrb.com/).

## Prerequisites

For this tutorial, you will need:  
**1. Resume**     
- You will need a resume in markdown format. Here is the link to a [quick tutorial](https://helloacm.com/markdown-markup-language-quick-tutorial/) on markdown.

**2. Static Site Generator**    
- You will need a static site generator to generate a static HTML website based on raw data and template. For this tutorial, we will be using [Jekyll](https://jekyllrb.com/) to create a static site. 

## Instructions

Once you fulfill all the prerequisites follow the below steps to host your resume.

**1. Creating a Repository on GitHub**  

- Because of its benefits: smooth concurrent work, ease of making changes without affecting other work, and most importantly better performance, distributed version control systems are mentioned by Andrew Etter. [Git](https://git-scm.com/doc) is the version control software and [GitHub](https://github.com/) is an online platfrom to store your files. [Login](https://github.com/login) to your GitHub account. If you don't have one create a [new GitHub account](https://github.com/join). 

    > * Click `+` on the right top corner of you GitHub account.
    > * Select `New respository` from the dropdown menu.
    > * Name the repository in `<username>.github.io`, this format should be followed to host your resume. (replace username with your GitHub username)
    > * Select the `public` option for visibility of the repository.
    > * Select `Add a README file under *Initialize this repository with*.
    > * Click on `Create Respository` button and your repository is created.  
    >  
    > ![](images/New%20Repository.gif)

**2. Create a local static site**  

- Etter praises the advantages of static site generators, praising their speed, portability, simplicity, and security. Ether mentioned that static sites don't require a server to run because they don't depend on server-side applications. We will use Jekyll to create a satic site. Install [jekyll](https://jekyllrb.com/docs/installation/) on your device. Once Jekyll is installed on your device follow the following steps to create a static site.  
      
    > 
    >* Open cmd and navigate to the directory in which you want to create your site.
    >* Use the following command to create a new Jekyll site. (replace username with your GitHub username)  
    >```
    >       jekyll new <username>.github.io
    >``` 
    >* Change into your new directory using following command.  
    >```
    >       cd <username>.github.io
    >```
    >* Build the site using following command. 
    >```
    >       bundle exec jekyll serve
    >```
    >* Open the browser and go to  [http://localhost:4000](http://localhost:4000) or navigate to the server address from the command prompt's output.   
    >  
    > ![](images/Local%20site%20host.gif)

**3. Locally Host your resume on that site**  

- You will need a resume in markdown format to host it on your static site. As mentioned by Ether in his book, you may still work on your website locally without an internet connection and then push the changes to the version control system as soon as you are finished and get internet access.
    >* Navigate to your static site folder and open `index.md` file
    >* Copy your resume file and paste it under the `index.md` file content.
    >* Use the command to rebuild your site.
    >```
    >       jekyll serve
    >````
    >* Open browser and go to  [http://localhost:4000](http://localhost:4000) or navigate to the server address from the command prompt's output to see your resume.   

    > 
    > ![](images/Host%20Resume.gif)

**4. Change the theme of the site**  

- The website has a very bland and unattractive appearance; we may improve it by changing the theme. There are numerous themes on [jekylltheme.org](http://jekyllthemes.org/) gallery. You can find more galleries on [Jekyll Themes](https://jekyllrb.com/docs/themes/) page. These modifications, which Etter discusses in his book, will make your work friendly and easier to read than mere lines of paragraphs.

    >* Select a theme from the galleries.
    >* Go to that theme's GitHub page.
    >* Follow the steps shown there.  
  
    > 
    > ![](images/Change%20theme.gif)

- *For some themes you will need more understanding of different technologies to use that theme.* 


**5. Host your resume on GitHub pages**    
- Once you are ready with an attractive site you are ready to host your resume using GitHub pages. As Etter points out, GitHub Pages leverages a production server as a remote repository, accomplishing the following: adding new files, updating existing files, and deleting outdated ones.

    >* Go to your newly created repository.
    >* Add the whole site folder to the repository which is created in [step 1](#instructions). Drag and drop it on your repository or add it by selecting the `Add file` option on your repository page.
    >* Write commite message under *Commit changes* section.
    >* Click on the `Commit changes` button to add your files.  
    >
    > ![](images/Host%20on%20Git.gif)


*Congratulations, your website has been hosted once all the steps have been followed correctly. Just go to the link `<username>.github.io` to view your site. (replace username with your GitHub username)*  

## More Recources

- Markdown:     [Markdown Cheatsheet](https://www.markdownguide.org/cheat-sheet), [Markdown Syntax](https://www.markdownguide.org/basic-syntax).  
- Jekyll:   [Installation Guide](https://jekyllrb.com/docs/installation/), [Ruby101](https://jekyllrb.com/docs/ruby-101/), [Creating Static site](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll).  
- GitHub:   [New GitHub Account](https://docs.github.com/en/get-started/signing-up-for-github), [Git Commands](https://confluence.atlassian.com/bitbucketserver/basic-git-commands-776639767.html), [GitHub Pages](https://pages.github.com/).

## Authors and Acknowledgments

- **Author:** Khush Patel  
- **Group Members:** Tanish sood, Juan Armijos, Chu Hao Wen  
- **Theme Credit:** [Hacker](https://github.com/pages-themes/hacker)
    

## FAQs
**1. Why is Markdown better than a word processor?**

- The key reason is that editing is simple on all platforms. To modify a markdown file, no specialized software is needed.

**2. Why is my resume not showing up?**
* There may be a variety of causes for this. Make sure to place your resume in the appropriate file **index.md**. For some themes, the location may change. To find the proper location, read the readme for that particular theme.  

* When you update the repository, wait a few minutes before viewing your resume because it could take some time for the repository to change.
