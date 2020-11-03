# App.js

We have a constant of shoes having objects which are shoes.

{Object.entries(shoes).map(([slug, {name, img}])=> <li key ={slug}></li> )}
1)We are converting each fo these shoes(objects) into entries.
2).map gives us an array so that we can map over each of the entries. In this array we have two elements 
    i). is the key(like "air-jordan-3-valor-blue)we are calling it slug in array or whatever you like.
    ii). Second is the value of each entries(name and img), we are destructuring it thats why placed in crly brackets.
3) => after arrow we define what we want to render. In this case we are returning li that has a key of slug and h2 which contains name of the shoe/entry and img tag having src of img 

We have defined all of this code in LaunchIndex component which is a children of Launch component but when we see DOM we are not getting the result. 
With nested Routes you need to tell the Parent Route to render the matching children it encounters, this is done using the <Outlet/> 

First we created the child component by the name of LaunchIndex which returned list of shoes. When we click on it nothing happened. We want to see the details of the shoes fo we created another Route by the name LaunchShoe with the path of ":slug" is the placeholder. 
We enclosed <li> in <Link> tag which link to slug (`lauch/$slug`)
slug is the name of the shoe
