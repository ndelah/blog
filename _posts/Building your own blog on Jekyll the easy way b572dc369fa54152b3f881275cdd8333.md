# Building your own blog on Jekyll the easy way

**TLDR:** Build a nice website using templates, zero knowledge in 10 minutes time.

## Why do we  need another tutorial on Jekyll?

There’s thousands of ways of making your blog. Using [Jekyll](https://jekyllrb.com/) is just one of the many options. 

Just like the website promises - or any other tutorial on the topic - it’s relatively easy to get started. The emphasis is on relatively. If you like the appeal of Jekyll but have next to zero experience with code it can be challenging to get started.

What I propose here today is the fastest way to set-up your blog using Jekyll if you have zero interest in reading any documentation. It’s not the cleanest way because you won’t necessarily fully understand how everything works, but you’ll know enough to mess. If every time you wanted to use a mode of transportation you had to build it, you’d probably walk everywhere. Some people have the time and patience to build a car, other just want to learn to drive.

Why would I do this? The Jekyll documentation is great but the **Getting started** section didn’t get me started fast enough imo. Sure it, helps you quickly make an empty site, but then you still have to read all of the documentation so you can build your entire site from scratch. 

## Prerequisites

- You made an account on Github
- You understand what [Github](https://kinsta.com/knowledgebase/what-is-github/) is. It’s a platform to share and host code. Think Google Drive for code.
- You understand what Jekyll is (it’s a tool for making websites).
- You understand that Jekyll and Github work hand in hand. Github Pages is a free service that allows your website to live on Github.

## Objectives and steps

**Objective:** Make and learn to use a simple blog based on a nice template someone else made. 

**Results:**

- Host the website on Github

**Steps:**

1. We install jekyll
2. We choose a template we like and “copy” and “paste” it to our computer
3. Host our website on Github
4. Add pages
5. Profit

### Step 1: Choosing a theme you like

There are [many places](https://jekyllrb.com/docs/themes/) to choose themes from, but we are trying to go fast so we’ll choose a theme from [this place](https://jekyllthemes.io/). If you want to go faster just pick [the theme of this blog](https://jekyllthemes.io/theme/contrast). 

Click the big `Get Contrast on Github` button. 

### **Step 2: Fork the Theme Repository**

You are now on the Github page of the theme. Someone made this, your job is to copy it to your own profile. The term for this is forking.

1. Go to the theme's GitHub page: [contrast](https://github.com/ndelah/contrast).
2. Click on the "Fork" button at the top right corner. This creates a copy of the repository in your GitHub account.

Your website will live Github through Github Pages. 

### **Step 3: Set Up GitHub Pages**

1. Go to your repository on GitHub.
2. Click on the "Settings" tab.
3. Scroll down to the "GitHub Pages" section.
4. In the "Source" section, select the branch you want to deploy. If you're using the main project structure, select **`master`** branch. Then, click "Save".
5. GitHub will now build your site and publish it. It might take a minute. Once done, GitHub will display a link to your published site.

… And you’re done. The website has been published and you can visit it. It isn’t exactly yours since you haven’t personalized it yet, but it is working and it’s the theme you chose.

### Step 3.5: Personalizing your website the fast and suboptimal way

You can edit your blog by directly modifying the files straight from Github or add files. All your blog posts are located in the `_posts` folder of your repository.  The posts are made using Markdown. Whenever you make a post , create a new markdown file that you add to the `_posts` folder. Copy the format of the file names `[YYYY-MM-DD-title.md](http://YYYY-MM-DD-title.md)` and copy the beginning of each file called the **frontmatter** that is at the top of the example files. 

Whenever you make changes to a Github repo whether to changes to a file (add, remove, updated, delete) you need to save those results. Github calls this making commits. 

Editing files on Github is fast for small changes but not convenient. The better way is to work with files locally on your computer using whatever tool you prefer to write markdown files then upload them to your github repo. 

### **Step 4: Clone Your Forked Repository**

1. Open your terminal.
2. Clone the forked repository to your local machine. Replace **`yourusername`** with your actual GitHub username.
    
    ```
    shCopy code
    git clone https://github.com/yourusername/contrast.git
    
    ```
    
3. Change into the cloned directory.
    
    ```
    shCopy code
    cd contrast
    
    ```
    

### **Step 3: Install Dependencies**

1. Make sure you have Ruby and Bundler installed. Then, install the Jekyll dependencies.
    
    ```
    shCopy code
    bundle install
    
    ```
    

### **Step 4: Customize Your Site**

1. Edit the **`_config.yml`** file in your site directory to customize your site's settings, such as **`title`**, **`email`**, **`description`**, **`author`**, etc.
2. You can create new posts by adding markdown files in the **`_posts`** directory. Follow the naming convention **`YYYY-MM-DD-name-of-post.md`** and the format provided in the example posts.

### **Step 5: Test Your Site Locally**

1. Serve your site locally to see how it looks.
    
    ```
    shCopy code
    bundle exec jekyll serve
    
    ```
    
2. Open a web browser and go to **`http://localhost:4000`** to preview your site.

### **Step 6: Push Changes to GitHub**

1. Add the changes to Git.
    
    ```
    shCopy code
    git add .
    
    ```
    
2. Commit the changes.
    
    ```
    shCopy code
    git commit -m "Initial blog setup with Contrast theme"
    
    ```
    
3. Push the changes to your GitHub repository.
    
    ```
    shCopy code
    git push origin master
    
    ```
    

###