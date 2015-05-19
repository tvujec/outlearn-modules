<!--
{
"name": "readme",
"version" : "0.1",
"title" : "Outlearn Hello World",
"description" : "Get Started with Your Path in 5 Minutes",
"homepage" : "https://github.com/outlearn-content/outlearn-modules",
"freshnessDate" : 2015-05-18,
"license" : "CC BY 4.0"
}
-->

<!-- @section -->

## How Fast Can You Publish?

### Viewing This on GitHub?

If you are viewing this on GitHub and want to get the full experience, check out the enhanced version of [Path Building Quick Start](https://demo.outlearn.com/learn/outlearn/my-outlearn-path) on Outlearn.com.


### Fork the Repo

We know you are busy and would rather focus on writing awesome content than setting up directory structures and choosing naming conventions. Never worry, you'll be all set with our [outlearn-modules](https://github.com/outlearn-content/outlearn-modules) GitHub repository. Your first step is to fork this repo. If you need a refresher on forking, check out GitHub's guide on [Forking Projects](https://guides.github.com/activities/forking/). They also have other handy [guides](https://guides.github.com).

<!-- @asset, "contentType" : "outlearn/prototype-feature", "text" : "{ \"task\": \"Fork the outlearn-modules repository. \"}"-->

Once you have forked the repository, open up `outlearn.json` found at the root of the repo. Update the following path metadata fields in the file:


| Field | Description |
| ----- | ----------- |
| name | used for the database, must be unique for your user account or organization |
| title | shown at the top of path cards |
| description | shown on the path card as additional information |

Your relevant part of your file should look like this:

```json
"paths" : [
  {
    "name" : "your-new-path-name",
    "title" : "The Name You Just Chose",
    "description" : "More explanation about your the glorious purpose of your path",
    "privacy" : "public",
    "pages" : [
      {"page" : "./pages/welcome.md"},
      {"module" : "readme"},
      {"module" : "my-outlearn-module"},
      {"page" : "./pages/specs.md"},
      {"module" : "outlearn/outlearn-markdown-specification"},
      {"page" : "./pages/closing.md"}
    ]
  }
],
```

<!-- @asset, "contentType" : "outlearn/prototype-feature", "text" : "{ \"task\": \"Update path metadata\"}"-->

<!-- @section -->

## Create an Outlearn Account and Publish Your Path

The best way for you to test out path creation on Outlearn is to see your changes in real time on outlearn. First, [create an Outlearn account using your GitHub account](https://demo.outlearn.com/auth/join). Click the button "Join With GitHub". You need to link Outlearn with GitHub so you can publish your content. GitHub will asks for your permission using a popup like the one below.

![GitHub sign-in popup](https://raw.githubusercontent.com/outlearn-content/outlearn-modules/master/images/authorize.png)

<!-- @asset, "contentType" : "outlearn/prototype-feature", "text" : "{ \"task\": \"Create an Outlearn account\"}"-->

Once you are signed up, choose [Import Content](https://demo.outlearn.com/import/github) from the menu in the top right corner under the user icon.

![GitHub import](https://raw.githubusercontent.com/outlearn-content/outlearn-modules/master/images/import.png)

Click "Add GitHub Integration" and choose "outlearn-modules" as the repository. Write a Nickname such as "Outlearn Modules" and click "Import Repository."

![GitHub import](https://raw.githubusercontent.com/outlearn-content/outlearn-modules/master/images/choose-repo.png)

You should now see "Outlearn Modules" under your "GitHub Integrations". Click on the it and then click on the green check under "Import History." You will see the imported paths and modules. Click on the path and you will see your first very own Outlearn path. Congratulations!

![GitHub import](https://raw.githubusercontent.com/outlearn-content/outlearn-modules/master/images/import-history.png)

<!-- @asset, "contentType" : "outlearn/prototype-feature", "text" : "{ \"task\": \"Publish your first path!\"}"-->

<!-- @section -->

## Add Your Content

### Pages and Modules

Now that you've laid out what your path is all about, it's time to get some content in it. Paths are made up of two basic components: pages and modules. The modules are the building blocks of a path. You might write them all yourself or you can include modules written by others. Each module should be self-contained so that it can be easily reused and reordered for other paths. To balance out the independence of the modules, you can put in pages. Pages are the glue that holds the modules together. They let you add in more of your own personality. Pages are specific to a path so you can talk about why you chose the modules you did, how they fit together, what parts are super important, etc.


### Outlearn Uses Markdown

We wanted to have an authoring experience that integrates seamlessly with GitHub and is easy as well as expressive. We think Markdown hits a great balance between those goals. You can read the [official Markdown Syntax](http://daringfireball.net/projects/markdown/syntax) for more details. Outlearn also supports all the extensions of [GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown/). If you already have your content in Markdown, importing it to Outlearn is a breeze.

### Hello World

By now you are probably itching to get to publish something you actually wrote. Go ahead and edit the file `welcome.md` in the `pages` directory. You can replace everything there with your very own "Hello World" message, or something else that inspires you! The pages are written in markdown so feel free to try out some formatting as well.

Now go back to the [Import Content](https://demo.outlearn.com/import/github) section on Outlearn, click on the nickname and then click "Re-Import". If you still have your path open, refresh your browser and you can see your edits. Or navigate to it same way as above. Houston, we have a lift-off! This is where the official 5-minute path publishing count stops. Hopefully you've seen enough of the power of Outlearn paths to keep on going to put some real content into your path.


### Organize Your Path

The meat of the path is in the modules. Once you have written some new markdown or repurposed older content, this is how you make it part of your path:

* Open the `my-outlearn-module.md` file in the `modules` directory
* Update the metadata at the beginning of the file, including a new name for the module, e.g. `awesome-first-module`.
* Add your markdown content to the file
* Save your file with a new name, we recommend using the module name also as file name, e.g. `awesome-first-module.md`
* Edit `outlearn.json` and replace `{"module" : "my-outlearn-module"}` with `{"module" : "awesome-first-module"}`. This tells the path where the module belongs.  
* Declare the module in the `modules` section in `outlearn.json` by replacing `"olm" : "./modules/my-outlearn-module.md"` with `"olm" : "./modules/awesome-first-module.md"`. This tells Outlearn where the source file for the module is.
* You can also remove the `README.md` module from the path.

The body of your `outlearn.json` will now look like this:

```json
"paths" : [
  {
    "name" : "your-new-path-name",
    "title" : "The Name You Just Chose",
    "description" : "More explanation about your the glorious purpose of your path",
    "privacy" : "public",
    "pages" : [
      {"page" : "./pages/welcome.md"},
      {"module" : "awesome-first-module"},
      {"page" : "./pages/specs.md"},
      {"module" : "outlearn/outlearn-markdown-specification"},
      {"page" : "./pages/closing.md"}
    ]
  }
],

"modules" : [
  {
    "olm" : "./modules/awesome-first-module.md"
  }
],
```

<!-- @asset, "contentType" : "outlearn/prototype-feature", "text" : "{ \"task\": \"Add your first module into the path.\"}"-->

### Including Images and Videos

Outlearn supports the regular markdown syntax for including images. However, you will get nicer rendering and better progress tracking using our own annotation. The Outlearn image annotation looks like this:

```markdown

< !-- @section, type: 'image/jpeg', title: 'Architecture Diagram', location: 'http://ad009cdnb.archdaily.net/wp-content/uploads/2011/05/1304980266-ad30-circulation-diagram.jpg' -->

```

You can add videos with the following annotations:

```markdown

< !-- @asset, type: 'video/vimeo', title: 'Watch the Video', location: 'https://vimeo.com/61887298' -->

< !-- @asset, type: 'video/youtube', title: 'Watch the Video', location: 'https://www.youtube.com/watch?v=CmjeCchGRQo' -->

< !-- @asset, type: 'video/mp4', title: 'Watch the Video', location: 'http://www.example.com/training/video1.mp4' -->

```

<!-- @section -->

## Enhance Your Content

### Adding Sections

The simplest way to enhance your content is to divide it into sections. Each module can have one or more sections that also show up on the side of the content and serve as a handy table of contents. They can also be checked off as completed and help learners and path creators see what progress has taken place.

You create a section by adding the following annotation:

```markdown
< !-- @section, "title": "Getting started" -->
```

Alternatively, you can leave out the "title" attribute and the platform will take the first heading after the section tag and make it the title. So you could replace the above code with:

```markdown
< !-- @section -->

## Getting Started
```

This can be especially helpful when you just quickly want to add sections to an existing markdown file and also makes the file render more nicely on GitHub.


### Add Tasks, Links

Nothing kills learner motivation like hours of watching videos and reading without a way to try it out yourself. Great teachers push the learners to put their learning to practice. The easiest way to create meaningful interactions with the learners on Outlearn is to add tasks, some of which may contain deliverables. A task can be as simple as "Run make in your project directory" or more involved such as "Download this library and compile it in your system." With deliverables, you get even more flexibility. For example, you can ask learners to "Fork the project repo on GitHub, add in your function and send a pull request to the original repo. Paste the url to the pull request below." Path authors and organization admins can see which tasks have been done and what learners have submitted. They can then organize further activities such as code reviews.

TODO: ADD IN SYNTAX

### Add Cover Images

Your path and each module in the path can have a cover image that's a visual representation of the path or module.
