---
id: button
title: Button Component
sidebar_label: Button
---

## Overview

The Button component is used to trigger an action or event, such as submitting a form, opening a dialog, or performing a task. It is a versatile element that can be customized in various ways to fit the needs of your application.

## Installation

To use the Button component, install the library:

````bash
npm install your-button-library

#Usage
import Button from 'your-button-library';

function App() {
  return (
    <Button onClick={() => alert('Button clicked!')}>
      Click Me
    </Button>
  );
}

#Props
The Button component accepts the following props:

Prop	Type	Default	Description
onClick	function	undefined	Function to call when the button is clicked.
label	string	undefined	Text to display inside the button.
disabled	boolean	false	Whether the button is disabled.
variant	string	'default'	The variant of the button (e.g., 'primary', 'secondary').
size	string	'medium'	The size of the button (e.g., 'small', 'medium', 'large').

#Variants
Examples of different button variants:

<Button variant="primary">Primary</Button>
<Button variant="secondary">Secondary</Button>
<Button variant="danger">Danger</Button>

#Sizes
Examples of different button sizes:

<Button size="small">Small</Button>
<Button size="medium">Medium</Button>
<Button size="large">Large</Button>

#Disabled State
An example of a disabled button:

<Button disabled>Disabled</Button>

#Custom Styles
To apply custom styles to the button:
import './custom-button.css';

<Button className="custom-button">Custom Styled Button</Button>

#Accessibility
The Button component supports ARIA attributes to improve accessibility. For example:

<Button aria-label="Close">X</Button>

#Examples
Comprehensive examples showing the button in various contexts:

// Example of a button used in a form
<form onSubmit={handleSubmit}>
  <Button type="submit">Submit</Button>
</form>

// Example of a button used to open a modal
<Button onClick={openModal}>Open Modal</Button>

#Troubleshooting
Common issues and solutions related to the button component:

Button not responding to clicks: Ensure that the onClick prop is properly passed and not undefined.
Button styles not applying: Verify that the correct CSS classes are being used and that there are no conflicts with other styles.

#API Reference
The Button component provides the following methods and events:

focus(): Focuses the button.
blur(): Removes focus from the button.
onClick: Event triggered when the button is clicked.


3. **Update Sidebar Configuration:**
   If you haven't already, make sure to include this new documentation page in the sidebar. Update the `sidebars.js` file in the `sidebars` directory. Add an entry for your new button documentation page.

   Example `sidebars.js`:

   ```js
   module.exports = {
     docs: [
       {
         type: 'category',
         label: 'Components',
         items: ['button'], // Add 'button' to the items array
       },
       // other categories or items
     ],
   };
````
