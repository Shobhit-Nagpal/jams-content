# HTML stuff
- HTML div element - used as a container
- divs are generic boxes that can contain anything
- <div> allows us to divide our page into sections and then use them for styling, etc
- id and class attributes
- Semantic HTML history

## Semantic HTML
- Accessibility (a11y)
- Web accessibility is where websites are designed in a way where they can be easily used by people with disabilities
- Disabilities can be from visual, hearing, psychological, etc

- We have elements that are a combination of:
    a. Semantic meaning but no context for tech that assists people with disabilities (<p>)
    b. Semantic meaning and has context (<button>)
- <div> and <span> are semantically neutral (no semantic meaning and no context)

## Landmarks
- HTML elements that act as regions of a page 
- 7 native HTML elements:
    1. <aside>
    2. <footer>
    3. <form>
    4. <header>
    5. <main>
    6. <nav>
    7. <section>

- These help people with assisitve technologies to navigate the website

# Styling

# CSS
- Cascading Style Sheets
- CSS is made up of various rules
- We select an element (through a selector), choose the property we want to style and give a value
Ex: 
a {
    color: blue;
}

## Selectors
- Selectors refer to the HTML elements to which the CSS rules apply to
- Types of selectors:
    i. Universal selector (*) - Select elements of any type
    ii. Type selector / Element selector(the tag itself) - Select all elements of given element type
    iii. Class selector - Selects elements with a given class
    iv. ID selecnt cantors - Selects elements with a given id

    Note: Eleme have only ONE id but multiple classes

    v. Grouping selectors - Can reduce code by applying same style to 2 selectors by grouping them 
    vi. Chaining selectors - Can chain selectors as a list without any separation (can chain class + class and also class + id) 
    Note: Can't chain the more than one element selector together like div p as it would literally try to find <divp>

- Combinators allow us to combine multiple selectors differently than either grouping or chaining them
- 4 combinators in total but we'll have a look at descendant combinator
- Descendant combinator (single space between selectors) - Will select element whose last selector matches with the selector of the previous selector. Like a parent with a child (a descendant)(Ex: .parent .child1)

## Properties
- color and background-color
- Typography and text-align
- Image height and width

## How to add CSS to HTML
1. External CSS
- With link tag in head
<link rel="stylesheet" href="./styles.css">
- Benefit of adding it externally:
    a. HTML and CSS is separated
    b. CSS can be edited from one place

2. Internal CSS
- With style tag in HTML (<style></style>)
- Used for adding unique styles for a single page of website
- Does not keep things separate

3. Inline CSS
- Adding styles directly to HTML elements
- No selectors being used
- Unique style to a single element then fine
- Generally not recommended

# Cascading of CSS
- CSS does what WE tell it to do
- Only exception to above rule is the default style that is given by the browser (which vary from browser to browser)
- Whenever we encounter unexpected behavior, it's cause of 3 main reasons:
    1. Default browser styles
    2. Not understanding how a property works
    3. Not understanding cascade

- Cascade is what determines which rules of CSS will be applied

## Main reasons of cascading
### 1. Specificty
- A CSS declaration that is more specific will take priority over less specific ones
- Order of specificity:
Inline styles > ID selectors > Class selectors > Type selector > Any other selectors
--> ID selectors > Class selectors > Type selector > Any other selectors

Note: When no declaration with a selector of higher specificity is there, the rule with greater number of selectors take place

### 2. Inheritance
- When a certain CSS rule is applied to an element and if that element has children / descendants, then the children will inherit style properties of the parent element WHEN there is not specific rule for the children themselves
- Typography-based properties are usually inherited, most properties are not

### 3. Rule order
- If specificity is not the problem and inheritance is not the problem, rule order comes in play.
- Rule order is basically where the last rule defined is applied

# Most important CSS skills to master:
- Positioning
- Layout

- Every thing on a HTML webpage is a rectangular box
Note: Put * {
    outline: 2px solid red;
}

-Many ways to manipulate the size of the boxes:
    1. margin (space between border of element's box and other element's boxes)
    2. padding (space of content in element from border of element's box)
    3. border (border adds space as well, even if it's by a pixel or two)

- Shorthand properties (allows us to set multiple values at same time, Ex: padding, border)

- Now, the issue with this is the actual space you define might be bigger than expected
- To solve this, we have an alternate box-model which we can enable by doing:
        box-sizing: border-box

- Example: https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/The_box_model#what_is_the_css_box_model

# Display property
- There are different display types which have unique box-models which we can modify by display property
- display: block && display: inline
- Most elements are block elements (elements stacked on top of each other)
- Inline elements do not start on a new line (appear on the same line)
- Ex: <p> is block but <a> is inline
- Also something called inline-block (inline behavior but block style padding and margin)

# Browser's default styles
- Chrome's default CSS: https://chromium.googlesource.com/chromium/blink/+/refs/heads/main/Source/core/css/html.css
- But we don't want default styles because different browsers might have different styles or we want to apply styles that conflict with the default ones
- We do a CSS reset or at the very least, reduce the default styles given by browsers

# Flex
- One of the most used tools as a web dev
- You HAVE to play around with flex box to get comfortable with it
- Flexbox is simply another way to arrange items into rows or columns
- The items can grow or shrink based on how you write the rules for them
- We have a flex container and flex items
- Flex container gets the property (display: flex)
- We can nest flex box as a concept
- flex: 1 (applied in flex item, is a shorthand for flex-grow [1] flex-shrink [1] flex-basis [0])
- flex: auto becomes (flex-grow [1] flex-shrink [1] flex-basis [auto])

## Flex directions
- Flex box has 2 directions (aka axes)
- Horizontal && Vertical
- Add flex-direction on the flex container
- Default value of direction is row
- Main axis defaults to horizontal

## Alignment in flexbox
- justify-content (align across main axis)
- align-items (align along cross axis)

## Gap
- Gap defines space between flex items in a flex box

Note: Interactive guide to Flexbox: https://www.joshwcomeau.com/css/interactive-guide-to-flexbox/

# CSS units
- Two types of units: absolute and relative units
- Absolute means units stays same in any context
- Relative means units differs according to context 
- px is an absolute unit
- em and rem are relative units

- em: font size of element OR (element's parent if we're using it to set font-sizes)
- rem: font size of the root element (:root or html)
- rem is usually recommended

- Also something called viewport units: vh and vw
- 1 vh = 1% of viewport height
- 1 vw = 1% of viewport width

# Topics to explore
- Responsiveness
- Grid
- More on accessibility
