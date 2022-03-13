## Understanding Tailwind-CSS - Part 1

Hey there everyone! I am finally back with some frontend stuff!

Spoiler Alert: I suck at frontend, but I am finally confident about talking about tailwind CSS!

Well, You might be thinking, What is there to talk about tailwind CSS, so, I will be Talking about what this thing is, will it replace bootstrap, Where to Use It, and a Small Demo 😅

Will try my best, even though I'm not great at it.

Let's keep going!🚀

### What's TailwindCSS?
So, If you have Used bootstrap before, you will find thousands of premade components, which you can just copy-paste, and adjust it according to your needs, isn't it, But Spoiler: With TailWindCSS, they Aren't available, So, it's totally utility based, where you have to Use the respective classes, and other styling Objects, and Make your website beautiful, and well-styled, and Moreover, Tailwind is utility-first CSS framework which promotes rapidly building custom designs So, you can build a website in no time, with or without using The Prototypes, if you have any, Cuz It's **AWESOME**, And moreover, When I discovered, tailwind, it was at it's early stages, and It's being Developed, and being made so Good, That I am dead sure it's **the CSS Of the Future!**, Even though it's quoted as "low-level CSS framework" It's easy to learn, and styles, and surely will make your site look lot better than the Crappy Bootstrap Styling, and People are tired of the old bootstrap layout 😂
In my opinion, the one thing that most developers will find a bit distracting with Tailwind CSS is the fact that your markup looks a lot busier than you might like. Tailwind isn’t the first utility CSS library, but it is the most popular at the moment.

### How is it Tailwind better than Bootstrap?
So, Everyone Knows
> Example is a Better Proof Than Words 

OKay, I know such Quote doesn't exist, But, it can 😂
So, Let's check out some bootstrap, and check out it's tailwind form!

#### Forms.
**Bootstrap**

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598371187537/d89ZSBOr-.png)
**Tailwind**

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598371207400/QCNoUNfmB.png)

#### Cards.
**Bootstrap**

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598371249515/F1DBmjckB.png)

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598371287547/ZFtcQdYp8.png)
**Tailwind**

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598371268811/jiFxkHzYI.png)

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598371302890/j9S3DS6jL.png)

#### Navbar.
**Bootsrap**

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598371375423/DnPEGppSU.png)
**Tailwind**

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598371357907/2IdtFduPC.png)

#### Results,
So after comparing what do you think, isn't tailwind Good and So beautiful?
But why, Is tailwind so Customizable that bootstrap, Because the creators, believe in The Utility classes, which enable Faster Prototyping, and Better styling.

Let's see the reasons why Tailwind is Better than Bootstrap now!
- Expanding default color palette
This new version of Tailwind comes with some upgrades to aid flexibility in using color shades by replacing the original seven-shade, darkest-to-lightest color system with a new nine-shade numeric color system, where 100 is the lightest shade and 900 is the darkest shade.

- Using progressive maxWidth scale
While we already had a linear scale for maxWidth (10rem), this new upgrade switches to a progressive scale where the value of the width increases and now has more default options from 9 to 12.

This default maxWidth scale can be overwritten by specifying the values you want for your own project in your config file:
```
module.exports = { 
  theme: { 
      maxWidth: { 
      // Your values for better styling, and overrides here.
    }, 
  },
}```
Oh, and i forgot  it is really stable and ready for production.

Also,
Your application doesn’t have a specific look like Bootstrap made projects. Tailwind CSS gives you a huge set of utility classes to build your own components or layouts.

Tailwind CSS itself is very huge. So if you load it from a CDN you end up fetching 1.4 Mbyte of CSS. Way bigger than other CSS Frameworks, so why do I use it in all my projects? Because it is utility-first. This means you can use a tool like Purge CSS in your build process to get rid of all the CSS definitions you don’t need and you end up with a very small CSS file.

Not to mention that you can optimize Tailwind CSS even more. If you use one specific group of classes again and again you can use the @apply directive to combine these classes to a new one

- **Is this really the future?**

Working with Tailwind CSS is using a set of utility classes that lets you work with exactly what you need. In my opinion, this is a neat way to create user interfaces that are more flexible to developers’ creativity.
Base set of components
In this case I must say that Bootstrap has a clear advantage because of its wide set of components including cards, modals, accordions, nav tabs and so on. Tailwind CSS has only a handful of components according to their documentation, the full list being:

- Alerts
- Buttons
- Cards
- Forms
- Flexbox grids
- Navigation
This compared to Bootstrap’ set of components. However, Tailwind CSS does have a lot more utility classes than Bootstrap does and using them you can create any type of component you want.

- **Performance**

Bootstrap has 4 files that are required to include into your project to get the full benefit of the CSS Framework. Together they amount up to 308.25kb including jQuery, Popper.js, Bootstrap JS and the main Bootstrap CSS file.

In comparison, Tailwind CSS only requires the base stylesheet file which amounts up to 27kb. It is true that Bootstrap has a much larger set of components and functionality, however if you don’t need certain components such as modals or accordions perhaps Tailwind is a better choice for more lightweight projects.

You can work in modules and there is no need for scoped css definitions anymore. Modularize your source code and rely on the defined classes of Tailwind CSS that don’t change. I love to structure my source code into components and for me the best component is if it is usable in every situation without any setup. To make this possible developers usually use the scoped option in your Vue js components to define css styles only for this specific component. But then you end up repeating yourself over and over so not the best practice. Wouldn’t it be great to have a reliable source of css style definitions that don’t change? Yes it would be great and Tailwind CSS is one way to solve this.

- **Community**

Bootstrap has been around for more than 9 years and being the most popular CSS Framework it has a large community of developers, forums, tools and so on. You can find countless of Stackoverflow threads answering to just about any question you might have about certain situations.

In the case of Tailwind CSS there is still much room to grow in terms of its community, however it is growing day by day and the number of tools and websites related to it are also increasing.

Another advantage I really appreciate  is and I am sure everyone would also Like is never having to worry about changes to one element affecting another related element. No more tabbing back and forth between HTML and style sheets in your editor, no more going back to check and see what you named that other element. In my opinion, this is the future.

### What is Utility First?
A utility-first library simply means that rather like Bootstrap, Tailwind doesn’t give us automatically pre-styled components. Rather, it gives us utility classes that help us style our component in certain ways and allows us to build our own classes using these utility classes. We'll See in the next Section, How Does it happen.

### A Large Demo!
I am gonna Show Designing a Form With Tailwind!
```css
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Static Template</title>
    <link
      href="https://unpkg.com/tailwindcss@^1.0/dist/tailwind.min.css"
      rel="stylesheet"
    />
  </head>
  <body>
    <div
      class="min-h-screen flex items-center justify-center bg-gray-50 py-12 px-4 sm:px-6 lg:px-8"
    >
      <div class="max-w-md w-full">
        <div>
          <img
            class="mx-auto h-12 w-auto"
            src="https://tailwindui.com/img/logos/workflow-mark-on-white.svg"
            alt="Workflow"
          />
          <h2
            class="mt-6 text-center text-3xl leading-9 font-extrabold text-gray-900"
          >
            Sign in to your account
          </h2>
          <p class="mt-2 text-center text-sm leading-5 text-gray-600">
            Or
            <a
              href="#"
              class="font-medium text-indigo-600 hover:text-indigo-500 focus:outline-none focus:underline transition ease-in-out duration-150"
            >
              start your 14-day free trial
            </a>
          </p>
        </div>
        <form
          class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4"
          action="#"
          method="POST"
        >
          <input type="hidden" name="remember" value="true" />
          <div class="rounded-md shadow-sm">
            <div>
              <label for="email">Email Address</label>
              <input
                aria-label="Email address"
                name="email"
                type="email"
                required
                class="appearance-none rounded-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-b-md rounded-t-md focus:outline-none focus:shadow-outline-blue focus:border-blue-300 focus:z-10 sm:text-sm sm:leading-5"
                label="Email address"
              />
            </div>
            <br />
            <div class="-mt-px">
              <label for="password">Password</label>
              <input
                aria-label="Password"
                name="password"
                type="password"
                required
                class="appearance-none rounded-none relative block w-full px-3 py-2 border border-gray-300 placeholder-gray-500 text-gray-900 rounded-b-md rounded-t-md focus:outline-none focus:shadow-outline-blue focus:border-blue-300 focus:z-10 sm:text-sm sm:leading-5"
                label="Password"
              />
            </div>
          </div>

          <div class="mt-6 flex items-center justify-between">
            <div class="flex items-center">
              <input
                id="remember_me"
                type="checkbox"
                class="form-checkbox h-4 w-4 text-indigo-600 transition duration-150 ease-in-out"
              />
              <label
                for="remember_me"
                class="ml-2 block text-sm leading-5 text-gray-900"
              >
                Remember me
              </label>
            </div>

            <div class="text-sm leading-5">
              <a
                href="#"
                class="font-medium text-indigo-600 hover:text-indigo-500 focus:outline-none focus:underline transition ease-in-out duration-150"
              >
                Forgot your password?
              </a>
            </div>
          </div>

          <div class="mt-6">
            <button
              type="submit"
              class="group relative w-full flex justify-center py-2 px-4 border border-transparent text-sm leading-5 font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-500 focus:outline-none focus:border-indigo-700 focus:shadow-outline-indigo active:bg-indigo-700 transition duration-150 ease-in-out"
            >
              <span class="absolute left-0 inset-y-0 flex items-center pl-3">
                <svg
                  class="h-5 w-5 text-indigo-500 group-hover:text-indigo-400 transition ease-in-out duration-150"
                  fill="currentColor"
                  viewBox="0 0 20 20"
                >
                  <path
                    fill-rule="evenodd"
                    d="M5 9V7a5 5 0 0110 0v2a2 2 0 012 2v5a2 2 0 01-2 2H5a2 2 0 01-2-2v-5a2 2 0 012-2zm8-2v2H7V7a3 3 0 016 0z"
                    clip-rule="evenodd"
                  />
                </svg>
              </span>
              Sign in
            </button>
          </div>
        </form>
      </div>
    </div>
  </body>
</html>
```
And the form Looks Like this

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1598373156445/M-BlOshPG.png)

Hope, you have got a Good Understanding, and I will Make another Blog, Teaching the basics, and working of Tailwind CSS, Till Then CYA

**Happy Hacking!**