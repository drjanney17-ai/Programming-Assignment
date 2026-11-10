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

## Bug Log (Part C)

| Bug | Function | What I Saw | Cause | Fix |
|---|---|---|---|---|
| C1 | welcomeMessage | ReferenceError: Name is not defined | Used `Name` instead of the parameter `name`. | Replaced `Name` with `name`. |
| C2 | isOnSale | Returned true incorrectly and changed the listing. | Used `=` instead of `===` for comparison. | Changed `=` to `===`. |
| C3 | cartSubtotal | TypeError when reading price. | Used `<=` instead of `<` in the loop condition. | Changed `<=` to `<`. |
| C4 | addTax | Returned undefined instead of the total. | Calculated the result without returning it. | Added `return rounded`. |
| C5 | addShipping | Returned "305" instead of 35. | Added a string instead of a number. | Converted the subtotal using `Number()`. |

## Reflection

This project was helpful to adjust to Javascript while being used to Java syntax. The `affordableTitles` function was the most difficult for me because it required combining several methods, variables, and function calls. It just made the overall process a little more challenging to understand and implement. I thought the bugs were all pretty simple to catch. 

## AI use statement

I used ChatGPT for organizing the assignment, Git instructions, and explaining some JavaScript concepts. I used it for guidance on managing my repository, commits, and project structure. 
