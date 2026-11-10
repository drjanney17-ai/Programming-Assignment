# PA2 — Book Swap Logic

**Name:** David Janney
**GitHub username:** drjanney17-ai
**GitHub Pages link for pa2/:** <!-- https://<username>.github.io/csdp232-pa1-<username>/pa2/ -->

## Project Overview

Shore Book Swap is a JavaScript project that manages textbook listings,
calculates prices, checks buyer affordability, and summarizes seller listings.

### Folder Structure

- `index.html` — Main project page and self-check interface.
- `css/checks.css` — Styling for the self-check page.
- `js/bookswap.js` — Part A and Part B functions.
- `js/buggy.js` — Part C debugging functions.
- `js/checks.js` — Automated self-checks.
- `js/data.js` — Sample book listing data.

## Testing Instructions

1. Open `pa2/index.html` in a web browser.
2. Open the browser Developer Tools using F12.
3. Select the Console tab.
4. Refresh the page.
5. Review the self-check results.

The project should pass all 37 automated checks across Parts A, B, and C.

## Self-check result

Self-check: 37 of 37 checks passed

## Bug log (Part C)

| Bug | Function | What I saw | Cause | Fix |
|---|---|---|---|---|
| C1 | welcomeMessage | Uncaught ReferenceError: Name is not defined | The parameter is `name`, but the return line used `Name`. JavaScript treats those as different names, so `Name` does not exist. | Changed `return greeting + Name + "!";` to `return greeting + name + "!";` |

| C2 | isOnSale | isOnSale(listing 101) returned true, and the listing's condition changed to "fair". Expected false, and the condition should stay "good". | `listing.condition = "fair"` assigns "fair" instead of comparing. An assignment used as a condition is treated as true, so the function always returned true and changed the listing. | Changed `if (listing.condition = "fair")` to `if (listing.condition === "fair")` |

| C3 | cartSubtotal | Uncaught TypeError: Cannot read properties of undefined (reading 'price') | The loop used `i <= cart.length`, so the last pass read one index past the end of the array. `cart[i]` was undefined there. | Changed `for (let i = 0; i <= cart.length; i++)` to `for (let i = 0; i < cart.length; i++)` |

| C4 | addTax | addTax(100) returned undefined. Expected 106. | The function calculated `rounded` but never returned it, so the result was undefined. | Added `return rounded;` after the rounding line |

| C5 | addShipping | addShipping("30") returned "305". Expected 35. | `subtotalText` is a string. Using `+` joined the text "30" with 5 instead of adding the numbers. | Changed `return subtotalText + shipping;` to `return Number(subtotalText) + shipping;` |

## Reflection

This project was helpful to adjust to Javascript while being used to Java syntax. The `affordableTitles` function was the most difficult for me because it required combining several methods, variables, and function calls. It just made the overall process a little more challenging to understand and implement. I thought the bugs were all pretty simple to catch. 

## AI use statement

I used ChatGPT for organizing the assignment, Git instructions, and explaining some JavaScript concepts. I used it for guidance on managing my repository, commits, and project structure. 
