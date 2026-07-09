# Overview
This is a tool I created back in 2020. I was using Markdown to write my course content and pushing it to GitHub. I would then copy and paste the content into Canvas, but OSU's version of Canvas strips out all the syntax highlighting on code snippets. You have to go in and manually update the HTML to recreate the syntax highlighting. There was a command line tool that I learned about from my dear friend Kevin McGrath that I started using (Pygments). I wanted something easier for me to use, and others, so I created this tool. It used to be hosted by an OSU AWS instance, but I never updated it to keep it from being depricated so it is no longer available. But, you can still download it and run it locally.

# Installation
Super simple, just clone the repo onto your computer `git clone https://github.com/ericianni/aws_pygments.git`. 

# Starting the server

Navigate into the directory where `application.py` is located and run it with `python3 application.py`. This should start the Flask app and it should list the address it is using: http://127.0.0.1:5000/. All you have to do is type that into your browser and you should be good to go!

# Functions
 At the top there is an instruction dropdown that will tell you everything this tool can do. I am also reproducing those below.

## Instructions
If you have a file containing the code you wish to highlight, you can upload it and have it automatically populate the form. You can also directly type or paste code into the form.

Once your code is ready in the text field, you need to set your options.

* **Language**: Auto will usually correctly identify the language, but sometimes you will need to set it yourself.
* **Color Scheme**: Select how you would like the final code to look
* **WCAG**8: None will use Pygments' built-in colors, but many of them do not pass Accessibility checks. It is recommended you us AA at the minimum.
* **Line numbers**: Toggle if you wish to display line numbers in a mobile friendly format.
* **Highlight lines*: If you need to draw attention to particular lines, you may use this option. Each line to highlight needs to individually typed with a space in between.
* **Bold everything*: Bolding can potentially increase readibility of individual letters, but may reduce how easy it is to parse the code.

After you have your options set, click the Highlight Code button. You will then see the raw HTML code you can use directly in Canvas along with how it will look. It is a good idea to check the preview to ensure the correct language was used to highlight the code. For ease of use, please use the Copy Text button. To use in Canvas, make sure you are in the HTML Editor and not the Rich Text Editor.
