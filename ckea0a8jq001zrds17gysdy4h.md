## Let's Learn API!

So, many of the people who have never hear of this term **API** might ask, 🤔What's this crappy thing stands for? So, API stands for **A**pplication **P**rogramming **I**nterface.

SO, we're gonna deep down explore APIs, and we'll be knowing about the following things:
- What are APIs
- What it does
- Benefits of API
- Implementation of APIs

So, without wasting any more further time, Let's get started! 😉

Let's start defining the Terms and Going Understanding them!

## Interfaces

Let's take the example of a simple old school Music players. They used to be so complicated to handle, and heavy to carry, even though such a simple interface which using to play music, which is it's prime job. It has the following states
- On / Off
- Volume High / Low
- Changing the source of Music
- Switching to a different Playlist
- Finding a favorite song of yours

But, when if you have ever tried to break, or see the inner components like me 😂You might have found out difficult to understand what are those, where are they connected to, how do they work, So, in simple words, when someone visits a website, they mostly see and interact with the frontend rather than the backend, which is rather useless to them.😄 And Moreover, you have the power to use frontend, and the magic of what's happening is always controlled by backend, so in regard to previous statement, even though someone can't control backend, doesn't render it useless.

And same thing goes for when something is being upgraded to a better working, or a better looking version, people still get new features to interact with, but there's no use of looking at the process going in the background.⚙

And finally These Interfaces become so nice looking, and good, they slowly turn into a Type of Interface called GUI, which stands for **G**raphical **U**ser **I**nterface

Simple Interface of Spotify Music Player:

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598356531893/LHD2ubzim.png)

![https___i.pinimg.com_originals_45_4c_4a_454c4a04248d6407d95558fc82293e70.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598356447474/UWD4hFguJ.png)

As you can see from both looks, how they adjust their interface to the screen size, and still has the same look, and feel, It's called interactive Interface.

And let's go in deeper, and take the example of the play button! When we click on the play button, what happens?

This happens:

![captured.gif](https://cdn.hashnode.com/res/hashnode/image/upload/v1598356711098/GrdHC_LoK.gif)
As you can see the state, and the respective state's icon changes from playing to pause, and back.

Basically, while coding, he just included the code from web, or local installed code, and used an handler, like the famous one `onEvent()` when the button is clicked, but he never implemented the code which is required to change the states, and attaching icons, and the hard work.

So, in fact, buttons are an essential part of the interfaces, which controls, the states, and state type, and on events, when the button is clicked, Whoa, so many things at once! 😁
And in this way, the developer has less work in implementing, and can reuse the same thing anywhere without hassle!

Also, one more thing, when designing a software, to make it reliable, and useful, and easier, a default api is provided by the OS too, which isn't directly used, and that's the reason, why programs have different running types on various Operating Systems, and we have docker to solve it, We'll Talk about it in Our next Article!

Let's see how the programmer uses the default api, without any knowledge:
```py
song_name = "hall-of-fame-song.mp3"
media_player = Media_player()

media_player.play(song_name)
```
Here we are not having to design the song loading, and the music player, being a part of the default api, and helping us to code faster by reducing the code, which we had to write if we need to make it ourselves, and hencing giving us a headstart, and better chance to work on the other features!

And one more thing, sometimes, program require you to install additional Libraries, another name for 3RD party APIs, and sometimes requires internet to run, because, they load the api from CDNs [Content Delivery Network] which stores the additional code, which is loaded which runtime, to ensure proper running of program using APIs.

This is how the interaction looks like:

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598358180105/s6gnMVl2I.png)

## Defining API

Let's dive into what are APIs and about them! Let's do it!😄

The term **API** are use to mostly refer to the web based application, and their endpoints, but that's not it, So, we will focus on all APIs, and their types, and show you, why the web based ones are so preferred by people, and used most!

And by the way, here's the link: [Click Me](https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API) To the Web Based AUDIO API documentation!

And most of the time while coding, we refuse to code the simple functions like making a string to upper case, or lower case, and just use the inbuilt functions aka APIs to speed up the coding process.

IF we do this to show the uppercase function:
```py
def uppercase(str_data):
    return ''.join([chr(ord(char) - 32) for char in str_data if ord(char) >= 65])

print(uppercase("abcd"))
```
It will be a waste of time and memory, which we can save by using the api like this:
```py
print("abcd".upper())
```
It's simple and faster right? 😎

Let's take another example, of files and it's handling in 2 different OS.
It might be `/home/user/Desktop` in linux, and `C:\Users\Admin\Desktop` in windows.

So, while working with files, the language we're working with provides us a kind of independence, which will work on any OS you expect it to:
```py
import os
dir = os.getcwd()

for entry in os.listdir(dir):
    print(entry)
```
And magically, this code works on any operating System, you expect it to!

So, now let's talk about web apis and the local ones.
When we want to edit something, we just install a package or an external library, and achieve it, and Boom! Our tasks' Done, But thinking of it, Let's say i am using another language, and implementing it isn't simple, so Web APIs come to the rescue, we provide a route to the api endpoint, where you can send the data, and get the result out of it, and moreover, the web apis can be accessed from anywhere, as it is hosted, and can be used to implement in any program, without caring about the language, or the framework stack we're using.

So, to sum up Definition of APIs, API stands for Application Programming Interface. It is basically how different machines and software talk to each other to create ever more complex applications. Even though APIs can simply refer to an interface to a local library, or the libraries themselves. For purposes of this website, APIs are assumed to be over the network to connect clients and servers (or multiple servers depending on your architecture and terminology).

#### Why make APIs, and What makes a Good API?
So, in this section, let's explore, why should we build and api, and the important characteristics, that makes an api Good, and better while using.

These days, very few applications are stand alone. If you build a mobile app, most likely you’ll need a build a server to provide resources for that mobile app. You’ll have to build internal APIs. And you’ll consume many third party APIs to avoid reinventing the wheel.

However, once you build an application that gains popularity, other developers and companies may also want to interface with it and leverage the technology or data. This can create a great opportunity to exponentially expand the influence of your company/organization. Your API is no longer just a tool to power your mobile app, but a product and a platform in it’s own right.

An API can act as a platform for new partnership opportunities, new revenue channels, or even new features for your organization. Many call this the API economy.

As thousands of developers integrate and work with your API, it may turn into your most valuable asset such as large companies like SalesForce and Expedia. In fact, Salesforce generates 50% of its revenue through their APIs, and Expedia generates over 90% of its revenue through their APIs. Today, billion-dollar companies like Stripe and Twilio has API products at its core.

And along with that, here are the important points, that makes a good API:
- Easy to learn
- Easy to use
- Hard to misuse
- Easy to read and maintain code that uses it
- Sufficiently powerful to satisfy requirements
- Easy to Extend
- Appropriate to the audience

#### Benefits OF APIs
Here are some point, that i Think, which Makes APIs useful!

- Automation: with APIs, computers rather than people can manage the work. Through APIs, agencies can update work flows to make them quicker and more productive.
 
- Application: because APIs can access the app components, the delivery of services and information is more flexible.
 
- More scope: with an API an application layer can be created which can be used to distribute information and services to new audiences which can be personalized to create custom user experiences.
 
- Efficiency: when access is provided to an API, the content generated can be published automatically and is available for every channel. It allows it to be shared and distributed more easily.
 
- Integration: APIs allow content to be embedded from any site or application more easily. This guarantees more fluid information delivery and an integrated user experience.
 
- Adaptation: needs change over time and APIs help to anticipate changes. When working with this technology, data migration is supported better, and the information is reviewed more closely. In short, APIs make service provision more flexible.

## Implementations of APIs

Hurray! You have finally reached the last Portion, where we're gonna fetch a simple API in Python 🤩 So lets get started!

So, we're gonna Fetch Data from a sample api, and know it how it works, So, we'll Fetch a Random Cat Picture, and Be sure to follow my steps along!

### Step 1: Open the website

so, the website we're gonna be using for our random Cat picture is [https://aws.random.cat/meow](https://aws.random.cat/meow) So, we will be visiting, but that's not it, in order, To get a random Image, we have to find the Endpoint,and Luckily this is the endpoint, but sometimes you have to find it! where we can Use a **GET** Request, Don't be confused, its a type of request, where Youre asking the web: "Knock knock, i am here! Can i have the random cat image please?" and he give the url, with a status code of 200, that means "Surely you may mister!" else, other codes, pose a different meaning, which I will surely explore later on!

When you visit, you'll see a JSON kind of response like this:

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598362341430/2BuAr0U7I.png)

Which means it's Working Successfully, Yay!

### Step 2: Fire up command console, and install fetching API!

Now it's time, we get the Images using Python, but we need a library named Requests which will help us Interact with The Web, SO, let's install it!

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598362445775/3YyKphjH_.png)
As you can see I already have it Installed, but if you don't It'll Be Installed!

#### Step 3: Get the Image URL!
Now We're Gonna Get the Image URL! and Print it, so Follow me Along!

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598362553521/G_OIOknpT.png)
So, here we import the newly installed request module, and perform get request with the `.get()` Method with the url endpoint as the input, and store it in the variable, now we need to check the status Code, if it's 200, then it's successful!

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598362630931/xSQEcpIXO.png)
So, as you can see, it gives me 200, that means fetching it is successful, now we need to convert the Request to JSON, and Parse it as dictionary, and extract the URL using the key.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598362680632/MB94-0PJh.png)
As you can see, The key to access is `file`

Now, we have safely parsed the request into JSON, and Used it like this:

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598362739246/qAblwrEzP.png)
 And next, we're gonna get the URL and Print it!

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598362769742/7Wq28DyjN.png)
And YAY! We did it!

### Download the Image!

Now after fetching, we have to Download the Image, so, what do we do?

We have to import the urllib3 module in python, and use it Like this:

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598362947616/OV397Hj0g.png)
And As you can see, the Image Has been successfully Downloaded! The Parameters are, the URL link of image, and the name of the file, you want it to be saved as. And now what's next? Navigate to the Folder and view the Image!

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598363052613/TgfZ-hOzG.png)
As you can see, it's been saved with the specified File name! Now i Hope you've understood, how to Use APIs In your Program, and Reduce you're code by a Lot, and Reuse the Fetched things!

Be Sure to Comment down your doubts, and your review, and I will be sure to reply!

Seeya For Now, Meet you in the next blog! :) **Happy Hacking!**