# What is NextJS?
+ A powerful framework for building fast and search engine friendly apps.
+ It is built on top on React
+ React is just a Library for UI
+ Nextjs is a combination of libaries, tools and conventions
+ It has its own routing library
+ Has its on compiler, CLI for building and running our apps, Has a nodeJS runtime.
+ We can build full stack apps using this
+ For react we need separate backend. But the nodejs runtime allows us server side rendering and makes it fast.

# Creating NextJS application
+ CMD to create nextjs app: npx create-next-app@13.4
+ Go to the project folder and to run it: npm run dev

# Project Structure
+ app folder: also called app router. The container for routing system.
+ public folder: contains the public assets like the images.

# Routing and Navigation
+ Routing is based on the file system
+ The routing system is based on convention and not configuration. So we should name of files correctly.
+ In the app folder, create a folder named user and in that create a .tsx file named page.tsx
+ In this file we should export a react component that will be rendered when the user goes to the /user url
+ We can also create nexted routes by creating a new folder named "new" inside the "user" folder and then create a page.tsx file in that folder. React component returned in that page.tsx file will be accessible at the /user/new URL.
+ For linked multiple pages, instead of using the <a> tag, which renders all the components of the page again, we use the <Link> component of the Next library. This will only rendere components that are required. This is called client side navigation.

# Client Vs Server Components
+ We have 2 env where we can render components and generate html markup. Either at the client-side within browser or the server-side within Nodejs runtime.
+ Client-side rendering is similar to react. Bundle all components and send to client. The larger the bundle the more memory we need at client side. No SEO. Less Secure. 
+ Server-side rendering sends smaller bundles (essential) to the client. Less resources needed at client. SEO. More secure. But, we lose interactivity (browser events - clicks, maintain states, access browser APIs).
+ Therefore we decide which components to keep at client side and which ones at server side.
+ Only keep components that has button clicks, or events on the client side.
![image](https://github.com/Zulelee/Learning/assets/106396856/2bb5a66d-0198-49ff-9767-1b444db0a59b)
+ In Nextjs, all components inside the App folder are server components by default.
+ To make a component client-side, just add 'use client' at the top of the file
+ Only make a component client-side when absolutely necessary. Instead of making an entire product card client component, only make the add to cart button a client component.

# Data Fetching
+ There are 2 ways we can fetch data, we can fetch it on the client or the server
+ To fetch data on the client, we use the two hooks: useState() to declare a state variable and useEffect() to fetch data and store it in state varibales.
+ Better is to fetch data on the server side.
+ We can get dummy data from -> https://jsonplaceholder.typicode.com/

# Caching
+ Caching is to store data somehwere it is faster to access.
+ We can store data in 3 places: Memory, File system or network.
+ Getting data from the network is slower than getting from the file system.
+ NextJS comes with a built-in data cache.
+ NextJS will automatically store data in the data cache that is based on the file system.

# Rendering
+ Performance optimization technique, also called static site generation.
+ If we have webpages that have static data, we can make nextjs render them once when building the application.
+ In comparison we have dynamic rendering, which renders the content at request time.
+ Both are done on the server side

# Styling NextJS application
## Global styles
+ global.css file in the app folder.
+ Use this for style that are global in our application.
+ Donot define custom classes here as they are only for specific components or page.

## CSS Modules
+ This is for a specific component/page
+ In the components folder, add a new file for the component for which you want to create the style sheet and keep the name same as the component and the extension should be .module.css

## Tailwind
+ A popular CSS framework
+ we have utility classes that we can use to style our applications

## DaisyUI
+ Component library for tailwind (bootstrap for tailwind)
