# Responsive Redesign

I redesigned the website for the Maine Historical Society in order to present a cleaner, more concise and accessible alternative.

<p align="center">
    <img src="./assets/development.png" alt="" width="1000">
</p>


## Table of Contents
* [Technologies Used](#technologies-used)
* [General Info](#general-info)
* [User Research](#userr-research)
* [Design Iterations](#design-iterations)
* [Features](#features)
* [Conclusion](#conclusion)
* [Project Status](#project-status)
<!-- * [License](#license) -->

## Technologies Used
JavaScript, Figma

## General Info
I chose to redesign the Maine Historical Society’s website as I have always been frustrated with many aspects of the front webpage. I have friends from Maine and have always been interested in learning more about the state's history. However, the website’s design makes it difficult to access important resources needed to learn more about Maine’s history and the MHS. I am eager to propose a sleek, simple, and improved redesign.

## User Research


Aleppo’s Sweets’ [website](https://www.alepposweets.com/) does not allow users to filter or sort their baklava items. As an avid baklava lover, I know exactly which baklava I prefer. However, many of my friends have never tried it before and struggle to choose one when asked to. They would appreciate a more sophisticated interface that would allow them to promptly choose one of the many items on the menu.

When taking a close look at the menu, I realized that the biggest factor that differentiated the items from each other was the main ingredient used. For example, customers who love pistachio will prefer to only look at the options with pistachio. I also noticed that two of the items off the menu are vegan and that vegan customers would appreciate it if they could sort the menu to only see these options.

<p align="center">
    <img src="./assets/baklava.png" height=400 alt="">
    <br>
    above: shows an example of the baklava menu on Aleppo’s Sweets’ website, in which there is no option to filter or sort items.
</p>


## Design Iterations

I initiated the design process by making the list of 12 items. On the first iteration, I had a separate page for my cart. However, I decided to place the cart on the page as the list of items as it would allow users to scroll through the list while also looking at their cart. Although this design choice makes the page a bit more cluttered, I think the trade-off is worth it as the main goal of designing this interface is to make the user experience easier.

## Features

### Usability Principles Considered
To make it easier for users to scroll through the list and update their cart at the same time, I made both the list of items and cart on the same page. I made sure that there was enough space for the image and description of the products so that the users can have a good look at them. I chose sorting by main ingredient type as a lot of people prefer walnuts over pistachios or vice versa. It is a big deciding factor. I also chose sorting by vegan/vegatarian as it is common for baklava stores to cater to people with different dietary resrictions. The filtering and sorting dropdown menus are all in one place to make the interface more useable and to make it easier for the user. 

### Organization of Components
ShopItem.js represents each individual baklava box item and has all the neccessary feilds. 
App.js has the rest of the app, including the shopping cart.

### How Data is Passed Down Through Components
Props are used to pass data from App.js to each individual ShopItem.js component. This data includes
the item fields and also the add to and remove from cart functions. The props are passed in from App.js
and accessed in ShopItem.js.

### How the User Triggers State Changes
When the user chooses a filtering option from the dropDown menu, the filter type (for filter 1 or 2) state changes. When the user chooses a sorting option from the sorting dropdown menu, the sorting type changes. The list of items that is displayed first gets filtered by functions matchesFilter1Type and matchesFilter2Type. If the user didn't choose any filtering in the dropdown menus, then the list will not be filtered. The cartList state changes when the user presses Add to Cart or Remove from Cart, for which their functions (contained within App.js) get called from ShopItem.js. Presing Clear Cart also triggers a change to this state (it makes the cartList empty).

## Conclusion

I was satisfied with the result in the end as it makes it easier for customers to choose items off the menu. I believe that Aleppo Sweets would benefit from implementing a similar interface on their website. 

## Project Status
Project is: Complete (as of December 2022)
