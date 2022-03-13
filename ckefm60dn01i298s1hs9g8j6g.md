## Python Packages for better development

Python packages make life easier, and they're exceptionally awesome. Making development faster and easier, I love it! The packages are stored in their own repository called PyPI, aka Python package index.

And Python is totally open sourced language, licensed under their own license, and even all of the Libraries, which we Use daily, And almost Thousands of ew libraries are added to PYPI and Since python has been dominating in a Lot of Tech Domains, It has all types of libraries, which you expect. So, to start, I have divided the List into categories, so you can refer easily, and Find your Specialized Domains.

The Categories to be found here are:
- Graphical User Interface
- Web Developement
- AI and Machine Learning
- Data Science, and Analysis
- Game developement
- Automation and Scraping

So, Lets Start!

## Graphical User Interface

### Kivy

Kivy is a special Framework, aimed at making android development portable and easy from the perspective of java developers, and using Kivy, and Python is lot easier, than using java.

And moreover, It also makes android developement cross platform, since, using Kivy, you can access it from any OS, such as windows, and MacOS, and the Final App, is also independent, as it Can run anywhere, on androids, and iOS too.

It's the One and Only Best framework in Python designed to make Android developement, faster, and better!

### Tkinter

This is the default GUI, which comes with Python, when you install it, and Opt for this. It has a Default Tk GUI Toolkit, which supports rapid designing, and better outputs, when used properly, But **WARNING**: This Framework isnt suitable, when you're making or working on a Large scale Production application, as the Animations, and Styling Which really Looks great, cannot be achieved to a great Extent.

Here's an Example Code:
```
from tkinter import *

root = Tk()

# Creating a Label Widget
myLabel = Label(root, text="Hello World!")
# Shoving it onto the screen
myLabel.pack()


root.mainloop()
```

### PyQt5

This is a Tool, specially Built by the QT company, who provides The GUI for any language, which has the ability to run on various OS and platforms, independently, achieving Perfect Cross Platform Independence.

Here's an example hello world!
```
import sys
from PyQt5 import QtCore, QtWidgets
from PyQt5.QtWidgets import QMainWindow, QLabel, QGridLayout, QWidget
from PyQt5.QtCore import QSize    

class HelloWindow(QMainWindow):
    def __init__(self):
        QMainWindow.__init__(self)

        self.setMinimumSize(QSize(640, 480))    
        self.setWindowTitle("Hello world") 

        centralWidget = QWidget(self)          
        self.setCentralWidget(centralWidget)   

        gridLayout = QGridLayout(self)     
        centralWidget.setLayout(gridLayout)  

        title = QLabel("Hello World from PyQt", self) 
        title.setAlignment(QtCore.Qt.AlignCenter) 
        gridLayout.addWidget(title, 0, 0)

if __name__ == "__main__":
    app = QtWidgets.QApplication(sys.argv)
    mainWin = HelloWindow()
    mainWin.show()
    sys.exit(app.exec_())
```

### PySide

There is an application / user interface (UI) framework written in C++ language called Qt (cute). Pyside is a wrapper of QT.

The difference with PySide is that PyQt is commercially available. And PySide, is good at Performace, but not at styling.

### PyGui

PyGUI targets Unix, Macintosh, and Windows platforms.
The focus of this MVC framework is to fit into the Python ecosystem with as much ease as possible.
And this is Not Great too for large scale applicationas, but relatively, easy to use and get started!

### Web Developement

### Django

As per the Django's Official Definition, it's The only Large scale web developement framework, that encourages rapid development and clean, pragmatic design. And It also Provides the basic tools, and Code, along with it's Own API, that Holds the tools, you frequently need to implement the features in a simple and robust manner.

Why is Django So popular:
- User Friendly
- Best to use when making quite large web apps
- Provides a neat set of tools, that speeds up developement
- Moderate to learn, easy to use

### Flask

Flask is a web development framework developed in Python. It is easy to learn and use. Flask is "beginner-friendly" because it does not have boilerplate code or dependencies, which can distract from the primary function of an application.

Some features which make Flask an ideal framework for web application development are:

- Flask provides a development server and a debugger.
- It uses Jinja2 templates.
- It is compliant with WSGI 1.0.
- It provides integrated support for unit testing.
- Many extensions are available for Flask, which can be used to enhance its functionalities.

Here's a simple hello world in Flask:
```
from flask import Flask
app = Flask(__name__)

@app.route('/')
def hello():
    return "Hello World!"

if __name__ == "__main__":
    app.run(debug=True)
```

### Tornado

Tornado is a Python web framework and asynchronous networking library, Which also provides the feature of Unblocking connections to the website, the program and the framework, handling every user Asynchronously. By using non-blocking network I/O, Tornado can scale to tens of thousands of open connections, making it ideal for long polling, WebSockets, and other applications that require a long-lived connection to each user.

Here's a Simple Hello world in Tornado:
```
import tornado.ioloop
import tornado.web

class MainHandler(tornado.web.RequestHandler):
    def get(self):
        self.write("Hello, world")

def make_app():
    return tornado.web.Application([
        (r"/", MainHandler),
    ])

if __name__ == "__main__":
    app = make_app()
    app.listen(8888)
    tornado.ioloop.IOLoop.current().start()
```

## AI and Machine Learning

### Tensorflow

Tensorflow, is a Free to use, and Open source Library for Machine learning, and neural networks research, Which is Produced, maintained By Google, and also used for Heavy research at Google, as a Part of their venturing Machine learning, AI and related fields.

Moreover, Instead of just focusing on Machine Learning, and AI, It also provides really best set of neat tools, for Total Scientific Computing and Mathematical Purposes.

### Pytorch

PyTorch is also an open source machine learning library used for developing and training neural network based deep learning models. It was  developed by Facebook's AI Team, and 

PyTorch works faster than Other Machine libraries Due to it's code optimzation, and the best algorithms and hence is more popular among Machine Learning developers. It also has A Good Api, that Helps to develop portable machine learning code, that is independent.

### Open CV2

OpenCV is an Amazing open-source library for computer vision, machine learning, and image processing.

It can process images and videos to find, every Minute details in the Videos, and search for Somethig specific like faces, or hadwriting if directed, with the Help of Machine learning

### Scikit-Learn

Scikit learn is one of the primitive machine learning frameworks, that's still Performing really good in this field, enabling users to get new features, and help them for rapid designing of models, and analyse them.

Why is it Good?
- Simple and efficient tools for predictive data analysis
- Accessible to everybody, and reusable in various contexts
- Built on NumPy, SciPy, and matplotlib
- It has the best algorithms in Classification, regression, and Clustering.

### Data Science and Analysis

#### NumPy

Numpy is a scientific Library For python, useful for Playing with Mathematics, or various Research, and Calculation In the field. It's quite famous, as it has several datatypes of it's own, which enables faster and optimized computing, which allows to code faster, without adding anything from scratch, and Provides some extravagant features. 

The following reasons makes it a Good library:
- It uses N dimesional Arrays, which are statically sized, enabling  the computer to perform better calculation with static sizes.
- NumPy offers comprehensive mathematical functions, random number generators, linear algebra routines, Fourier transforms, and more.
- The core of NumPy is well-optimized C code. Enjoy the flexibility of Python with the speed of compiled code.
- NumPy’s high level syntax makes it accessible and productive for programmers from any background or experience level.

### Scipy

Like Numpy, Scipy is also a Great library, written in C for python, used for scientific purposes. So, basically, it's an arsenal of Scientific tool for Researchers. The Scipy ecosystem is a collection of open source software for scientific computing in Python.
Scientific computing in Python builds upon a small core of packages:

Python, a general purpose programming language. It is interpreted and dynamically typed and is very well suited for interactive work and quick prototyping, while being powerful enough to write large applications in.

The SciPy library, a collection of numerical algorithms and domain-specific toolboxes, including signal processing, optimization, statistics, and much more.

### Pandas

Pandas is a Data analysis Library, that heps you research and play with Huge amounts of data, minify them, by extracting nto group, and analyzing the data to use the results for several purposes. A fast and efficient DataFrame object for data manipulation with integrated indexing is present in pandas, which makes it more awesome for data analysis, and minifying into chunks with it.

Here are some of the remarkable features:
- Tools for reading and writing data between in-memory data structures and different formats: CSV and text files, Microsoft Excel, SQL databases, and the fast HDF5 format.
- Intelligent data alignment and integrated handling of missing data: gain automatic label-based alignment in computations and easily manipulate messy data into an orderly form.
- Flexible reshaping and pivoting of data sets.
- Intelligent label-based slicing, fancy indexing, and subsetting of large data sets.
- Columns can be inserted and deleted from data structures for size mutability.

### Matplotlib

Matplotlib is a mature and popular plotting package that provides publication-quality 2-D plotting, as well as rudimentary 3-D plotting.

It's famous for it's graph plotting features in advanced manner, and it consists of 3 Main Factors:
- **Create**: Develop publication quality plots with just a few lines of code
Use interactive figures that can zoom, pan, update.
- **Customize**: Take full control of line styles, font properties, axes properties.
Export and embed to a number of file formats and interactive environments.
- **Extend**: Explore tailored functionality provided by third party packages

## Game Developement

### PyGame

Pygame is a Gaming engine for Python, that enabes you to develope cross platform video games. It also enables making graphics, and adding sound effects for realistic game dev which istead uses the SDL library, included in pygame SDK.

The applications which use pygame as the main engine, have an advantage, they can be run on any PC OS, or even mobile Phones!

### Turtle

Turtle is a default graphical user interface like tkinter, that is shipped with python by default, and enabling them to play with art, and designs, and even make games
with the canvas provided to draw within.

It also enables to make graphics, and various other things for using in programs, or making amazing shapes, and other things.

Here's the simulation of virus, using turtle:
![A Virus](https://cdn.discordapp.com/attachments/737338096483565578/748899111268384768/unknown.png)

## Automation and Scraping

### Requests

Requests is a Library that's made with the motto of **"HTTP For Humans"** which enables people, to interact with the web, and apis consisting of HTTP, in an easy way, which can be understood by us, and even how the HTTP works.

It enables us to do things, that we're not able to do Manually, Like
- Sending Headers
- Sending Post Requests
- Sending authentication key for authorization

Here's an Example of scraping an API:
```
import requests

req = requests.get("https://mrwinson.me/api/jokes/random")

# Extract json
data = req.json()

# Get the joke
joke = data["joke"]

print(joke)
```

### Beautiful Soup 4

This library comes in handy, When you can't use an API for a website's endpoint, r it doesn't exist, then Beautiful Soup helps to analyze the Website, and Find the required data in the html page. And Moreover, it also supports pulling the contents from XML files too with the new update.

And in brief, Web scraping is a useful method that is used to extract useful data of a website by extracting the HTML of the website when You can't use JSON APIs.

## Some extra tidbits!

### What are Microframeworks?

Micro-frameworks are the opposite of full-stack frameworks, which also offer additional modules for features such as authentication, database ORM, input validation and sanitization, etc.

####Why is CherryPy and Flask considered Microframework?

Flask and CherryPy are known as a micro-frameworks because they are lightweight and only provides components that are essential. It only provides the necessary components for web development, such as routing, request handling, sessions, and so on. For the other functionalities such as data handling, the developer can write a custom module or use an extension. This approach avoids unnecessary boilerplate code, which is not even being used.

Hope this was quite informative for you all. If you liked it, let me know in the comments. See you next time! :)