# Prep Network Navigation & Aggregator Exercise

## Overview

This exercise will have the candidate build a responsive site navigation driven by an AJAX request.

Here are the guidelines for this exercise:

-   1) Create a new instance of Wordpress and install the Sage Wordpress Starter theme included in the resources folder.
-   2) If needed, utilize the theme documentation: https://roots.io/sage/docs/theme-installation/.
-   3) Build and design the site navigation utilizing an ajax request with the included json file.
-   4) Build and design one post aggregator using the WP Rest API found here - https://www.prephoops.com/wp-json/wp/v2/posts
-   5) Place the javascript for both of the above tasks in /resources/assets/scripts/routes/common.js.
-   6) In the resources/views folder, create a new front-page.blade.php file and place the necessary HTML there.
-   7) Aggregator must include 3-5 posts and each post must have the title, featured image, and a link to the post.
-   8) Chrome compliance is all that's required, all functions and features available in Chrome are in play.
-   9) Nav must be responsive.
-   10) Complete the challenge and return the updated theme files that include the functionality for the menu and post aggregator.

At a high level, the navigation will have two main states

-   <768px: Mobile. Hamburger icon will display in the top-left of the page. Clicking the hamburger will cause a card to slide in and overlay the content from the left. The card will contain nav and sub-nav items defined in the JSONP response
-   \>= 768px: Desktop. The nav will display as a horizontal nav. Top level nav items will display sub-nav items when clicked. No hamburger will be shown.

## Version

0.1.0

## Files

-   Mockup - Illustrator file describing how the nav should behave can be found in the resources folder

## API

-   There is a folder called "data" which contains a JSON file for you. Use it however you'd like, but make sure the content of the site's nav comes from the JSON and is not hardcoded.

## Get Started

```
git clone git@github.com:JeanHules/prephoops-frontend-challenge.git
cd prephoops-frontend-challenge/react-starter-template
cd app
yarn
yarn dev
The url will show in terminal for where you can view the site.
```

## Design Specifications

### Typography

-   **Primary Navigation** 21/48 PrepHoops Avant Garde Bold
-   **Secondary Navigation** 16/48 Galaxie Copernicus Book
-   **Headline (Desktop)** 120/132 PrepHoops Avant Garde Bold
-   **Body Copy (Desktop)** 24/36 Galaxie Copernicus Book
-   **Headline (Mobile)** 44/48 PrepHoops Avant Garde Bold
-   **Body Copy (Mobile)** 14/24 Galaxie Copernicus Book
-   **Copyright (Mobile)** 12/16 Helvetica Neue Regular

### Color

-   **Orange** #f76517
-   **Light Gray** #eee
-   **Translucent Black** rgba(0, 0, 0, 0.5)

### Measurements

Measurements are specified in pixels. Dimensions are fluid unless specified.

### Interactions

#### Desktop

-   On hover, Primary Navigation reverses color (white/orange).
-   On click, if item contains a URL, Primary Navigation navigates to a new page.
-   On click, if item contains other items, Secondary Navigation appears (see Desktop, Secondary Navigation).
-   Menu appears containing Secondary Navigation.
-   Translucent mask appears over content, behind menu.
-   On hover in, Secondary Navigation changes color (orange/light gray).
-   On click, Secondary navigates to a new page.
-   On click outside of menu, menu and mask are hidden.

#### Mobile

-   When a user clicks the open navigation icon (“hamburger”), the navigation should “push” from left to right.
-   The PrepHoops logo and navigation toggle slide left to right.
-   The open navigation icon should change to the close navigation icon (“x”).
-   Translucent mask appears over content, right of navigation.
-   The Primary Navigation should include link items and menu items.
-   When a user hovers a Primary Navigation item, it should change color (orange/light gray).
-   When a user clicks a Primary Navigation link item, the browser should navigate to a new page.
-   When a user clicks a Primary Navigation menu item, the Secondary Navigation should “push” down, the chevron should rotate \* 180°.
-   When a user hovers a Secondary Navigation item, it should change color (orange/light gray).
-   When a user clicks a Secondary Navigation item, browser should navigate to a new page.
-   When a user clicks outside of the navigation, the navigation should close.
-   When the navigation closes:
    -   the menu should “pull” from right to left
    -   the logo and toggle button should “slide” from right to left
    -   the close icon should change to the open icon
    -   the mask should be hidden
