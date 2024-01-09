/** Finding the Path **/

E7 P4 - TOPICS

## How to keep the Header intact and only the Body changes depending on the page

- When we have / -> we need to have Home, If we have /about -> we should have About

> We have to create Children routes of the AppLayout
> We make use of children routes which is a list and contains a list of paths

const AppLayout = () => {
return (

<div className="app">
<Header />
{/** if path = / \*/}
<Body />
{/** if path = /about _/}
{/\*\* if path = /contact _/}
<Footer />
</div>
);
};

{

    path: "/",
    element: <AppLayout />,
    children: [
      {
        path: "/body",
        element: <Body />,
      },
      {
        path: "/about",
        element: <About />,
      },
      {
        path: "/contact",
        element: <Contact />,
      },
    ],
    errorElement: <Error />,

},

> We need to push the children according to the route
> So, react router gives us a component called "Outlet"

## outlet

> This called as a Named import from the react-router-dom
> We need to create a <Outlet />
> Outlet is in the AppLayout, whenever there is a change in this path, the outlet will be filled with the children according to the path
> For instance, if we are in /about then the outlet will be filled with about us page, same for the others
> We can have multiple parents and children
> We will never see this <Outlet /> in the HTML, Its replaced by the component according to the path

## How do we create a link to Home, About ... when we click on it?

> Never use a anchor <a></a> tag in react because the entire page gets refreshed
> We can navigate to a new page without reloading the entire page

## link component

> We will use a component called link - superpower given to us by react router dom
> link works exactly like the anchor tag

<a href="path">Contact US</a>
Syntax:

<Link to="path">Contact US</Link>

## That is why our applications are called as SPAs(Single Page Applications)

> It is whole single component, all the routing/new pages are just components just interchanging themselves
> We dont reload our website

## Two types of routing

> Client-side routing
> Server-side routing

# Server-side routing

> We have a index.html, about.html, contact.html if we click on the anchor tag (/about) it reloads the entire page and sends a network call to about.html, fetches the HTML from the server and renders our page
> This is called as server-side routing

# Client-side routing

> Here what we do in our application is the client-side-routing
> No network calls are made, all components are already loaded the first time
