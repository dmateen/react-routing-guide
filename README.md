# The Ultimate Guide to React Router: Everything You Need to Know


Welcome to this beginner's guide to React Router, a powerful routing library designed for React applications. 

In this article, we'll take you through the fundamentals of React Router, offering an easy-to-understand approach for handling navigation and routing. Whether you're new to routing or looking to grasp the basics of creating single-page applications with multiple views, React Router is an excellent starting point.

## What is React Router?

React Router is a powerful routing library for React applications. It allows you to handle navigation and routing in a declarative way, making it easier to create single-page applications with multiple views. Whether you want to handle simple routing or implement complex nested routes, React Router has got you covered.

## Getting Started with React Router

Before we dive into the details, make sure you have React Router installed in your project. You can install it using npm or yarn by running the following command:

```shell
npm install react-router-dom
`````

Once installed, you can import the necessary components from `react-router-dom` and start using React Router in your application.

## Basic Routing with React Router

Setting up basic routing in React Router is a breeze. Here's a step-by-step guide to help you get started:

1. Wrap your entire application in the `BrowserRouter` component. This component enables HTML5 push state-based navigation.
2. Define your routes using the `Route` component. Each route is associated with a specific path and renders a component when that path matches the current URL.
3. Use the `Link` component to create navigation links. This component ensures that the URL is updated, and the corresponding component is rendered when clicked.

Wait! Lets go though the things step-by-step
# Detailed Steps for Setting Up React Router

Let's break down the steps to connect your application to the browser URL using `BrowserRouter`, create Routes, and finally, create links to these pages:

## Step 1: Connect your application with the browser URL
To establish a connection with the browser URL, start by using the `<BrowserRouter>` tag. This tag enables various features, such as navigating using `URL/about`, `URL/contact`, and more. To utilize these features, you will first need to import `BrowserRouter` from `react-router-dom`. 

By including this import statement in your code, you unlock the powerful routing capabilities provided by React Router. This empowers you to effortlessly create dynamic and navigable web applications. Take advantage of this functionality to enhance user experience and streamline navigation.

```jsx
import { BrowserRouter } from "react-router-dom";
```

Then, wrap it around your App in the index.js file:
```jsx
<BrowserRouter>
  <App />
</BrowserRouter>
```
Alternatively, you can move to your App.js file and wrap it there:

```jsx
function App() {
  return (
    <BrowserRouter>
      {/* Your components and routes go here which we will create in the next step*/}
    </BrowserRouter>
  );
}
```

Now we are connected to our Browser URL.Which means we are done with the first step which can help us navigate through our application


## Step 2: Create Routes
Next, we need to create Routes. 
Create a `Routes` tag and define all the routes within that tag. A `Route` tag, within the routes, will define the path and element. 

The element here defines the thing or component that needs to be published as soon as we move to a specific URL, like `url/about`:
```jsx
<BrowserRouter>
  <Routes>
    <Route path="/" element={<div>Home Page</div>} />
    <Route path="/about" element={<div>About</div>} />
    <Route path="/contact" element={<div>Contact</div>} />
  </Routes>
</BrowserRouter>
```


## Step 3: Create Pages
To enhance your application, create three pages: 
1- Home.js 
2- Contact.js
3- About.js. 
These pages will serve as key components of your website, providing valuable information and functionality to your users. 
Update your routes accordingly to ensure seamless navigation and accessibility. By incorporating these pages into your application, you will be able to provide a comprehensive and engaging user experience.

```jsx
<BrowserRouter>
  <Routes>
    <Route path="/" element={<Home />} />
    <Route path="/about" element={<About />} />
    <Route path="/contact" element={<Contact />} />
  </Routes>
</BrowserRouter>
```
By now, we have connected our application with the Browser URL and have also defined what needs to be displayed when a URL is hit - the Pages!

## Step 4: Create Nav Bar 
So, we are done with
- Connecting to URL using the BrowserRouter
- We have defined all the Routes in the <Routes> tag
- We have created the pages where we want the user to be navigated

Now, lets create a Header Component, containing Navbar, that will be included in every page.

Create a list where your list items will have a link to the pages:
```jsx
<header>
  <ul>
    <li>
      <Link to="/">Home</Link>
    </li>
    <li>
      <Link to="/about">About</Link>
    </li>
    <li>
      <Link to="/contact">Contact</Link>
    </li>
  </ul>
</header>
```
And now, we have our Header, including the Links, ready to be incldued in every page
I won't go into styling this list as this is not the primary purpose of this guide. 


## Step 5: Update `Link` to `NavLink`
Update the `Link` to `NavLink`, as it adds the active class there, which will show that a particular link is clicked:
```jsx
<header>
  <ul>
    <li>
      <NavLink to="/">Home</NavLink>
    </li>
    <li>
      <NavLink to="/about">About</NavLink>
    </li>
    <li>
      <NavLink to="/contact">Contact</NavLink>
    </li>
  </ul>
</header>
```
That's all! You have successfully set up React Router in your application. 


Happy coding!
