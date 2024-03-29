# How to host and format a resume using Markdown, GitHub Pages and Jekyll (On Windows)

## Purpose

- Host and format a professional resume using Markdown, GitHub Pages and Jekyll.
- Understand and incorporate the general principles of current Technical Writing, as explained in Andrew Etter's book Modern Technical Writing.

## Prerequisites

- [A GitHub Account.](https://docs.github.com/en/get-started/signing-up-for-github/signing-up-for-a-new-github-account)
- A Resume formatted in Markdown.
- [Git installed](https://git-scm.com/downloads)

## Modern Technical Writing: An Introduction to Software Documentation, by David Etter
David Etter's book, "Modern Technical Writing: An Introduction to Software Documentation," provides guidance for creating effective and maintainable documentation. He suggests using lightweight markup languages and static site generators, integrating documentation with engineering code, and storing documentation in distributed version control systems. Etter also emphasizes the importance of contributions from subject matter experts, testing and researching extensively before writing, and publishing documentation on websites instead of PDFs for up-to-date information. By following these practices, technical writers can create useful and accessible documentation that supports the needs of their users.
## Instructions

1. Use lightweight markup
2. Use Distributed Version Control
3. Make Static Websites

Now, we can get started and use these principles as a guideline.

### Install Ruby and Jekyll

1. Install Ruby

- Open [RubyInstaller](https://rubyinstaller.org/downloads/) and download the newest version of Ruby WITH DEVKIT.
- Select all default options for installation.
- Run the `ridk install` at the end of the installation wizard.
- Select the option `MSYS2 and MINGW development tool chain`.

2. Install Jekyll

- Open a new command prompt by typing in `cmd` on the search bar of your computer.
- Type `gem install jekyll bundler`.
- Type `jekyll -v` to assure it was downloaded correctly.

### Download and edit a resume theme

1. Find a theme and edit it
- Go to [RubyGems](https://rubygems.org/).
- Search "Jekyll resume theme".
- Click on any resume theme that might interest you.
  - I used [Alembic](https://jekyllthemes.io/theme/alembic).
- Click "Homepage" under links to view and download the theme.
- Scroll down until you reach README for further instruction on the given theme.
  - Note: Some themes require you to have already created a static site, so I will quickly show you how to set that up.
- Open a new command prompt by typing in `cmd` on the search bar of your computer.
- Enter the folder where you saved the static website to by typing `cd "foldername"`.
- Type `jekyll new resume`.
  - Note: "resume" can be any name you'd like.
- Follow the instructions of the README of the theme you chose to go with. This will include editing the theme as well.

2. Run the static website theme locally
- Open a new command prompt by typing in cmd on the search bar of your computer.
- Enter the folder where you saved the static website to by typing `cd "foldername"`.
- Type `bundle install`.
- Type `bundle exec jekyll serve`.
- Copy the server address and post it into a web browser.
  - Server address: http://127.0.0.1:4000/

![gif1](https://github.com/martinpopper/martinpopper.github.io/blob/main/7e8mti.gif)
![gif2](https://github.com/martinpopper/martinpopper.github.io/blob/main/7e8mc1.gif)

### Host your resume on GitHub Pages

1. GitHub
- Go to [GitHub homepage](https://github.com/).
- Log in and locate the main page.
- Click Create a new repository.
- Choose a name for the repository.
  - Note: It may be easier to name the repository the same as your website. (In this case, resume).
- Keep all default settings and create the repository.

2. Edit YML file
- Open your documents and locate the folder of the resume that will be hosted.
- Open the config.yml file.
- Locate the line that says `baseurl:` and type in the name of the repository you just created.

3. Git commands
- Open a new command prompt.
- Use `cd`to change into the folder you will be using to host on.
- Type `git init'
- Then `git checkout -b gh-pages`
- Then `git add .`
- Then `git commit -m "anyMessageYouWant"`.
- Go back to GitHub and copy the link to the right of "git remote add origin".
- Go back to the command prompt and type in `git remote add origin link` where link is the link you just coppied off GitHub.
- Type `git push origin gh-pages`.

## More Resources

- [MarkDown tutorial](https://www.markdowntutorial.com/)
- [Modern Technical Writing: An Introduction to Software Documentation - Andrew Etter](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS)
- [GitHub Pages Documentation](https://docs.github.com/en/pages)

## Authors and Acklowedgments
- [David Darnes](https://github.com/daviddarnes): Creator of Jekyll theme used
- Aditya Kashyap 
- Akashkumar Ghelani 
- Saif Mahmud 

## FAQs
- Why is Markdown better than a word processor?
  - Markdown helps to enforce consistent formatting and styling across different documents. This is particularly useful for technical writing, where consistency and clarity are important.
- Can I use an older version of Ruby?
  - Yes! However the instructions for installation might be different. 
