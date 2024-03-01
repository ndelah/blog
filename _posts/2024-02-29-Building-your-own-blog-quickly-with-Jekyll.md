---
title: "Building your own blog on Jekyll the easy way"
layout: post
---

**TLDR:** Build a nice website using templates, zero knowledge in 10 minutes time.

## Why do we  need another tutorial on Jekyll?

With countless methods to craft a blog, Jekyll offers one such path. Despite its learning curve for beginners, this guide aims to expedite the process for those eager to bypass extensive documentation reading.

The approach here isn't about mastering Jekyll's inner workings but rather achieving a functional blog setup swiftly. It's akin to driving a car without needing to build it from scratch—ideal for those prioritizing speed over detailed understanding.

Why this guide? While Jekyll's documentation is comprehensive, its Getting Started segment falls short in rapid deployment, especially for complete novices desiring an immediate and tangible outcome.

## Prerequisites

A GitHub account creation.
Familiarity with GitHub, the code hosting and sharing platform.
Basic understanding of Jekyll as a website creation tool.
Knowledge that Jekyll and GitHub integrate seamlessly, with GitHub Pages offering free website hosting.

## The approach

The objective is to launch a simple blog using an existing template.

After this quickstart you will have learned:

- Where to find templates
- How to "download" them and host them on Github
- How the website is published
- How to edit the very basics of your website in a quick and dirty way on Github
- How to edit your blog post on any editor locally and "upload" (commit) them to Github.

What you **won't** learn:
- the specific structure of features of every template
- Fundamental features of Jekyll.
- The basics of Git versioning.

**Steps:**

1. We choose a template we like and “copy” and “paste” it to our computer
2. We install jekyll
3. Host our website on Github
4. Add pages (on Github Directly)
5. Add pages locally

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

YEdit or add files directly on GitHub for immediate updates. Blog posts reside in the _posts folder, using Markdown format. Follow the naming and frontmatter conventions shown in example posts. Remember, changes on GitHub require commits to save.

For substantial edits, work locally and upload changes to GitHub for a smoother experience.

### **Step 4: Clone Your Forked Repository**

1. Open your terminal.
2. Navigate to the directory where you want to keep your blog

    ```sh
    cd ./directory_name/sub_directory_name
    ```

2. Clone the forked repository to your local machine. Replace **`yourusername`** with your actual GitHub username.
    
    ```sh
    git clone https://github.com/yourusername/contrast.git

    ```
    
3. Change into the cloned directory.
    
    ```sh
    cd contrast    
    ```

### **Step 3: Install Dependencies**

1. Make sure you have Ruby and Bundler installed. Then, install the Jekyll dependencies.
    
    ```sh
    bundle install
    gem install bundler jekyll
    
    ```

### **Step 4: Customize Your Site**

1. Edit the **`_config.yml`** file in your site directory to customize your site's settings, such as **`title`**, **`email`**, **`description`**, **`author`**, etc.
2. You can create new posts by adding markdown files in the **`_posts`** directory. Follow the naming convention **`YYYY-MM-DD-name-of-post.md`** and the format provided in the example posts.


### **Step 5: Push Changes to GitHub**
Imagine you're working on a digital scrapbook on your computer, where you've just added some new pages or made changes to existing ones. To update the online version of your scrapbook (so everyone else can see the changes), you need to follow a few steps using Git, a tool that helps manage different versions of your project.

1. Add the changes to Git.
    
    ```sh
    git add .
    ```

This command is like telling your computer, "Hey, take a snapshot of all the changes I've made to my scrapbook." The dot here means "everything in this folder," so it's a quick way to grab all the updates you've made.

    
2. Commit the changes.
    
    ```sh
    git commit -m "Initial blog setup with Contrast theme"
    ```

 Now that you've taken snapshots of your changes, you need to put them in a photo album so they're organized and labeled. This command does just that. The -m stands for "message," where you describe what changes or updates you're adding to the album. 


    
3. Push the changes to your GitHub repository.
    
    ```sh
    git push origin master
    ```


Finally, you want to share this updated photo album with your friends and family online. This command uploads your new album to the online version of your scrapbook, so everyone can see the latest changes. "Origin" refers to the online storage location for your scrapbook, and "master" is like the main version of your scrapbook that everyone sees.

## You're done
You're done, you've set-up your blog. Enjoy writing and sharing your articles. 