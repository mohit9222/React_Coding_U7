/** Finding the Path **/

E7 P5 - TOPICS

# Dynamic routing

> Dynamic route for every resturant
> Changes based on each route (dynamically)
> We want to uniquely create this resturant
> This means :resId is the dynamic part (Every resturant over here will be unique) - Routes will be unique

{
path: "/resturants/:resId"
},

## How do we read the resId

> We use hook which is superpower called "useParam()" hook which comes from react router dom

## Link

> It is a special component which is given to us by react router dom
> behind the scenes link is using <a> tag
> Wrapper over the anchor tag -> link
