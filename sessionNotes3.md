/** Finding the Path **/

E7 P3 - TOPICS

## Routes

> We need to use a Javascript library called "React Router DOM" (Version 6+)
> ? How do we install this React router library?

- We will use npm i/install react-router-dom

# Features we are going to build

> If we type localhost:1234/about -> this should take us to the about page
> Same thing for the other pages like Home, Contact, Cart

# Routing Configuration

> When ever we have to create routes, we have to create a routing configuration
> We will create the routing configuration in the root level of the app (App.js file)
> We will need a Named Import called "createBrowserRouter from the "react-router-dom"
> createBrowserRouter will create the routing configuration

# Configuration

> It means some information that will define what will happen on a specific route(URL)

# createBrowserRouter

> This will take a list of "PATHS"(object)
> If the path is "/" then we load the element -> home

const appRouter = createBrowserRouter([
{
path: "/",
element: <AppLaout/>
},
{
path: "/about",
element: <About />
},
{
path: "/contact",
element: <Contact />
}
])

> This will not help by just configuring it on the page, it needs to be rendered
> We need to provide this configuration to render it
> We will call another component called "RouterProvider"

# RouterProvider

> RouterProvider will provide this routing configuration to our app
> Earlier we where rendering the <AppLayout/> directly

root.render(<RouterProvider router={appRouter} />);

We can also use other Routers but its best to use "createBrowserRouter" - NOTE

if we type localhost:1234/anything - This will throw an unexpected app error

# Create our own Error page /handle erros

> we can also have a errorElement: which runs the error component

{

    path: "/",
    element: <AppLayout />,
    errorElement: <Error />,

},

> React gives a router hook for our router which is called the "useRouteError"

# useRouteError()

> This is called using a named import called useRouteError

import { useRouteError } from "react-router-dom";

> when ever we see a function starting with "use" it is a hook (IMP) (Common convention)
> Gives us more information about the error and show specific details to the user

const err = useRouteError();
