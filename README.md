# How to Host an Online Resume the Right Way With Help From Andrew Etter
### I. Purpose:
1) To describe the practical steps of how to host and format a resume using Markdown, the Apostrophe Markdown Editor, GitHub Pages, and Jekyll.
2) To relate the practical steps described above to the general principles of current Technical Writing, as explained in Andrew Etter's book *Modern Technical Writing*.

### II. Prerequisites
- a markdown-formatted essay (seem *More Resources* for help with this)
- a GitHub Account
- a markdown editor such as Apostrophe
- Jekyll (built into GitHub)

### III. Instructions
#### 1) Create your resume
The first thing we need to do is to create a resume, and we will be using the markup language Markdown for this. See the *More Resources* section for instructions on how to use markdown.

Using Markdown has significant advantages for us, both for writing this resume as well as for general technical writing. As Etter explains, its simplicity makes it easy to learn in just a few minutes, whereas a traditional markup language like XML can take weeks to learn, and years of experience to master. Markdown also has the advantage that it is easily readable in its raw, plain text form, which makes for much easier review and editing down the road. 

#### 2) Create your GitHub repository

1) In your GitHub Account, under *Repositories*, click "New"
2) On the *Create a New Repository* page, input the repository name as *YourGithubUsername.github.io*.
3) Make sure that the repository is set to public, and that the options *Add a README file*, *Add .gitignore*, and *Choose a license* are not checked.
4) Click on *Create Repository*

![Gif showing how to create a repository](https://github.com/joe7057/joe7057.github.io/blob/main/create%20a%20repository%20named%20as%20yourgithubusername.github.io.gif?raw=true)

One of Etter's key suggestions for technical writing is to use a distributed version control system. GitHub is an implementation of the git version control system, freely available to anyone who wants to use it. Many companies will have their own internal git servers, but either way, the important thing is to have version control. This gives significant advantages to both the technical writers and the end users. For the writer, they can easily make and track changes to their documentation, and git takes care of many problems that can arise when multiple writers are updating the same documentation repository. For users, especially developers, if they see an issue with the documentation, they can submit a pull request for the issue rather than having to directly contact the specific writer who created the documentation. Version control systems are also excellent for documenting why each change to the documentation was made via commit messages. 

Using the same version control system for your documentation as is used for the program you are documenting can also be beneficial. As Etter points out, this can allow the versions to be easily paired between the code and the documentation, which is a godsend for end users who are using an older version of the software and need the documentation that applies to that version. I'm sure we've all had that one time where we are stuck using an older version of some piece of software, and are struggling to find a solution to some problem that isn't specific to the newest version. 

#### 3) Upload your resume

1) In the new repository, click *Add File* and select *Upload Files*
2) Drag your resume markdown file, named *index.md*, into the upload boc
3) Add a commit message and press *Commit Changes*.

![Gif showing how to upload your resume file](https://github.com/joe7057/joe7057.github.io/blob/main/in%20the%20repository,%20click%20add%20file%20and%20upload%20your%20index.md%20file%20in%20to%20the%20repository.gif?raw=true)

#### 4) Choose your Jekyll theme

1) In your repository go to *Settings* -> *Pages*.
2) Under *Theme Chooser* click *Choose Theme*.
3) There is a list of GitHub default Jekyll themes. Choose one and click *Select Theme*.

![Gif showing how to choose a Jekyll theme in GitHub pages](https://github.com/joe7057/joe7057.github.io/blob/main/in%20your%20repository%20go%20to%20settings%20-%20pages%20and%20click%20choose%20theme.%20Choose%20the%20theme%20you%20want%20from%20the%20github%20default%20jekyll%20themes.gif?raw=true)

Another of Etter's recommendations is to use static sites, and more specifically to use a static site generator. Static sites are great because they are so simple and lightweight. There is no backend, no messy database or constant connection requirement. They really are the way the internet is supposed to be. Just download a file, and there is the web page you wanted to see. 

While it is possible to create a static site by hand, in the modern world we use static site generators. These tools allow you to provide your content in lightweight markup, while the formatting information is specified as a separate set of templated HTML and CSS. Run the generator, and it will put the two together and spit out a nicely-formatted static site ready for publication (if you did it right, see *More Resources* below). This not only makes it easy to populate a site with content quickly (especially if you want multiple pages with different content but the same layout, such as the pages of a documentation site), but it also makes it extremely easy to update. All you have to do it make the desired changes to the markup content, and re-run the generator to get the updated site. 

#### 5) That's it! Your resume is live!

To view your published resume, you can go to *YourGithubUsername.github.io*. This is the same as the name of the repository we created earlier. 

![Gif showing how to view the published resume](https://github.com/joe7057/joe7057.github.io/blob/main/go%20to%20yourrepositoryname.github.io%20to%20view%20your%20resume.gif?raw=true)

### IV. More Resources

- [Markdown Tutorial](www.markdowntutorial.com)
- [CloudCannon's Jekyll Tutorial](https://cloudcannon.com/community/learn/jekyll-tutorial)
- [*Modern Technical Writing* by Andrew Etter](https://www.amazon.ca/Modern-Technical-Writing-Introduction-Documentation-ebook/dp/B01A2QL9SS/ref=sr_1_1?dchild=1&keywords=andrew+etter&qid=1635903320&sr=8-1)

### V. Authors and Acknowledgements

Author: Joseph Smith

Jekyll Template *Slate* by GitHub. Taken from github.com/pages-themes.

Credit to the other members of group 4 for their suggestions and feedback. 

### VI. FAQs

1) Why is markdown better than a word processor?

	Word processors such as Microsoft Word are excellent at exactly one thing: creating documents for export to pdf. They include all sorts of fancy formatting tools that make it easy to format your document while you are writing it. The problem is that they store these formats in a complex, often-proprietary format. Since we know from reading Etter's book that we want to use a version control system, this will not work for us because these document formats do not play nice with versioning (unless it is their own proprietary version, which we don't want). In contrast, markdown is a completely plaintext format, and therefore is perfectly suited for use with version control software. Markdown (or similar markup languages) is also required for the use of static site generators such as Jekyll, so if we want to publish our documentation as a site, word processors simply aren't an option. 

2) Why should I take the time to create a Jekyll template when I could just convert my markdown file to html directly?

	One of the benefits of markdown is its ability to be easily converted to html for quick writing of webpages. However, markdown is quite limited in its formatting capabilities, especially as compared to writing in html directly. You can include html tags inline in markdown, but then you are missing the point of using it in the first place. Using a Jekyll template lets you add much better formatting to your webpage, and as you learn more about it, you will find that you can be even more creative by adding data via .yml files rather than markdown, for proper, professional applications suitable for publication to your client/employer's customers. 

3) Why isn't my resume showing up?

	Make sure that you named your resume file *index.md*. This is the filename GitHub's built-in jekyll is programmed to look for when creating the static site. It should be located in the repository's root directory. 

4) Do I have to use GitHub's simplistic pages? I want to do something more complex.

	Not at all! The demonstration in this tutorial was intended as a simple introduction to publishing with Jekyll and GitHub pages. You are welcome to design a more complex Jekyll template and publish it on GitHub pages. For this application, I would recommend setting up a local git repository linked to GitHub, and installing Jekyll on your machine for local development and testing. You'll be amazed at what you can do with these amazing tools. Godspeed!










