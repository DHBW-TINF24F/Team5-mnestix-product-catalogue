# The shopping cart feature

This document specifies the requirements for the shopping cart functionality of the Mnestix Browser Extension.

## General Requirements

**[SC-GR-01]** The shopping cart view shall is accessible under `/cart` route.
**[SC-GR-02]** The shopping cart features shall add new data structures. Note: Use existing AAS-product model where applicable.
**[SC-GR-03]** The shopping cart shall persist data using the existing local storage mechanism.

## Menu Bar Integration

**[SC-MB-01]** The menu bar shall display a cart icon that indicates the number of items in the cart.
**[SC-MB-02]** Clicking the cart icon shall navigate the user to the shopping cart view.
**[SC-MB-03]** The cart icon shall update in real-time as items are added or removed from the cart.
**[SC-MB-04]** An empty cart shall not display a badge with item count.

## Shopping Cart View

**[SC-SCV-01]** The shopping cart view shall display a list of products added to the cart, including product name, quantity, price per unit, and total price.
**[SC-SCV-02]** The total price is displayed at the bottom of the shopping cart view.
**[SC-SCV-03]** Each product in the cart shall have a "Remove" button to delete the item from the cart.
**[SC-SCV-04]** The quantity of each product can be adjusted using a numeric input field or increment/decrement buttons (max. 9999 items).
**[SC-SCV-05]** The view shall contain a "Checkout" button. Note: the actual checkout process is out of scope for this document.
**[SC-SCV-06]** If the cart is empty, a message "Your cart is empty" shall be displayed and a button to navigate back to the product listing page shall be provided.
**[SC-SCV-07]** The shopping cart view shall be responsive and usable on both desktop and mobile devices.

## Shopping Cart Integration

**[SC-SCV-01]** A new product can be added to the cart from the product detail view (`viewer`) by clicking an "Add to Cart" button.
**[SC-SCV-02]** After adding a product to the cart, the user shall decide to either stay on the product detail view or navigate to the shopping cart view.

## Administration Requirements

**[SC-AR-01]** A flag to enable/disable the shopping cart feature shall be available in the config files (Docker).
**[SC-AR-02]** The URL path for the checkout process (external) shall be configurable in the config files.

## Other Requirements

**[SC-OR-01]** The shopping cart shall be available in three languages: English, German, and Spanish.
**[SC-OR-02]** The translations for the shopping cart feature shall be stored in the existing localization files.
