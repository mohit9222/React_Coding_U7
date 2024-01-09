/** Finding the Path **/

E7 P1 - TOPICS
useState and useEffect Hooks - Diving deep
useEffect()
When is useEffect() called?

---

## useEffect()

> The useEffect is called using a Named Import from the react library
> It takes two arguments 1. -> callback function 2. -> Dependency array (optional)

## When is useEffect() called?

> useEffect is called everytime after the component is rendered
> In other words, after the component has finished rendering, useEffect is called.
> Dependency array changes the behaviour of its render
> If NO DEPENDENCY ARRAY, the useEffect will render everytime the component renders
> If DEPENDENCY ARRAY is EMPTY [], the useEffect is called on only INITIAL RENDER(just once)
> If DEPENDENCY ARRAY has a value [btnNameReact], then useEffect is called everytime btnNameReact is updated/changes

> The basic nature or default behaviour of useEffect is to be called after each render (IMP)
