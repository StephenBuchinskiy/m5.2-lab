# web-dev-starter

This is a starter project for web development with no frameworks and minimal
dependencies. It is intended to be a starting point for web development projects
that are written in plain HTML, CSS, and JavaScript.

## Getting Started

To get started, clone this repository and run the following commands:

```bash
npm install
```
This will install the necessary dependencies for the project.

## Development

It is recommended to use the VSCode Live Server extension to run the project
locally. This will allow you to see changes in real-time as you make them. There
is no need to run a build process or refresh the page manually. Additionally,
you do not need to setup a local server to run the project.

## Testing

This project does not have updated tests, meaning this section can be skipped.

To run the tests for the project, run the following command:

```bash
npm test
```

## Accessibility Lab Questions

# Color

The main background and the green grid boxes do not pass the test, and the black text color over the green background also fails the WebAIM test. I fixed this issue by changing the box colors to straight white (#FFFFFF). This now passes all the tests.

# Semantic HTML

1) You can use the arrows to move up and down the page. Tab works to swap selection of different elements, but cannot select "Show comments". Tab also skips over all headings and paragraphs in the article. It doesn't look like you can select the links under the "Related" tab, and images are also unselectable.

2) To make it easier for screen reader users to navigate, I added . I updated the article text by getting rid of the "br" elements and replacing them with "p" elements for each paragraph section. I also replaced the "font[size="?"]" elements with the appropriate section headings. I also replaced the "td" elements in the table header with "th" elements. 

3) The 'div class="nav"' should be updated to just be a "nav" element, with the css styles applying to this nav element and not 'div class="nav"'.

# The Images

I added alternative text to each image that summarizes what the image is portraying.

# The Audio Player

1) To provide accessibility to hearing impaired individuals, I added a transcript section with a heading and a paragraph that contains the transcribed audio right below the player.

2) To provide accessibility for older browsers, I added an option that displays that the browser doesn't support displaying the audio file. Right below this, there are two download options for the audio file, one in MP3 and the other in OGG.

# The Forms

1) To make the input invisible to users but visible to screen readers, I created a label element with its own CSS class that virtually hides the label while making it still accessible to screen readers. I did not add the hidden attribute as that would make the label invisible to both users and screen readers.

2) I made the two comment input elements unambiguously associated with their labels by adding a label element for each input field and tying those labels to the respective input fields by adding the "for" attribute. This ties each label to its input for screen readers.

# The Show/Hide Comment Control

I was able to make the button keyboard-accessible by switching the div element to a button element. This allowed the existing button css rules to take effect and for the javascript functions to correctly show and hide the comments.

# The Table

To solve the table issue, I added a hidden caption describing the table that is still accessible by a screen reader. I also added scopes to each column and row header so that screen readers can inform listeners which cells are headers and which ones are actual values within a respective column/row.

# Other Considerations

1) Adding functionality that makes it easier for keyboard users to tell where the currently selected element is. This will make tabbing through the webpage faster and more responsive.

2) Making the text bigger, specifically the paragraphs, so that people with poor vision will have an easier time reading the contents without needing a screen reader. Another option for this is adding an interactable font-size changer so that users can select their desired font-size.

# Sources

https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Accessibility/HTML
https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Accessibility/Multimedia
https://github.com/mdn/learning-area/blob/main/css/styling-boxes/styling-tables/punk-bands-complete.html
ChatGPT