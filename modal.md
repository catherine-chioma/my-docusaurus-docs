---
id: modal
title: Modal Component
sidebar_label: Modal
---

## Overview

The Modal component is used to display content in a layer above the main content. It can be used for dialogs, lightboxes, and other temporary content.

## Installation

To use the Modal component, install the library:

````bash
npm install your-modal-library

#
Writing documentation for a modal component using Docusaurus involves creating a comprehensive markdown file that describes the modal's usage, props, examples, and other relevant information. Here's a step-by-step guide:

Create or Open a Documentation File:
If you haven't already, create a new markdown file in the docs directory of your Docusaurus project. You can name it modal.md. If a file for the modal documentation already exists, open it.

Write the Documentation:
Use the following template to create a detailed documentation for your modal component.

Here's an example modal.md file:

markdown

---
id: modal
title: Modal Component
sidebar_label: Modal
---

## Overview

The Modal component is used to display content in a layer above the main content. It can be used for dialogs, lightboxes, and other temporary content.

## Installation

To use the Modal component, install the library:

```bash
npm install your-modal-library

#Basic Usage
Here’s a basic example of using the Modal component:
import React, { useState } from 'react';
import Modal from 'your-modal-library';

function App() {
  const [isOpen, setIsOpen] = useState(false);

  return (
    <div>
      <button onClick={() => setIsOpen(true)}>Open Modal</button>
      <Modal isOpen={isOpen} onClose={() => setIsOpen(false)}>
        <h2>Modal Title</h2>
        <p>Modal Content</p>
        <button onClick={() => setIsOpen(false)}>Close Modal</button>
      </Modal>
    </div>
  );
}

#Props
The Modal component accepts the following props:

Prop	Type	Default	Description
isOpen	boolean	false	Whether the modal is open or not.
onClose	function	undefined	Function to call when the modal is closed.
title	string	undefined	Title of the modal.
children	node	undefined	Content of the modal.

Variants
Examples of different modal variants:

import Modal from 'your-modal-library';

// Info Modal
<Modal isOpen={isOpen} onClose={handleClose} variant="info">
  <h2>Info Modal</h2>
  <p>This is an info modal.</p>
</Modal>

// Warning Modal
<Modal isOpen={isOpen} onClose={handleClose} variant="warning">
  <h2>Warning Modal</h2>
  <p>This is a warning modal.</p>
</Modal>

// Error Modal
<Modal isOpen={isOpen} onClose={handleClose} variant="error">
  <h2>Error Modal</h2>
  <p>This is an error modal.</p>
</Modal>

#Custom Styles
To apply custom styles to the modal:

import './custom-modal.css';

<Modal isOpen={isOpen} onClose={handleClose} className="custom-modal">
  <h2>Custom Styled Modal</h2>
  <p>This modal has custom styles.</p>
</Modal>

#Accessibility
The Modal component supports ARIA attributes to improve accessibility. For example:

<Modal isOpen={isOpen} onClose={handleClose} aria-labelledby="modal-title" aria-describedby="modal-description">
  <h2 id="modal-title">Accessible Modal</h2>
  <p id="modal-description">This modal is accessible.</p>
</Modal>

#Examples
Comprehensive examples showing the modal in various contexts:

import React, { useState } from 'react';
import Modal from 'your-modal-library';

function Example() {
  const [isModalOpen, setIsModalOpen] = useState(false);

  return (
    <div>
      <button onClick={() => setIsModalOpen(true)}>Show Modal</button>
      <Modal isOpen={isModalOpen} onClose={() => setIsModalOpen(false)}>
        <h2>Example Modal</h2>
        <p>This is an example modal.</p>
        <button onClick={() => setIsModalOpen(false)}>Close</button>
      </Modal>
    </div>
  );
}


Writing documentation for a modal component using Docusaurus involves creating a comprehensive markdown file that describes the modal's usage, props, examples, and other relevant information. Here's a step-by-step guide:

Create or Open a Documentation File:
If you haven't already, create a new markdown file in the docs directory of your Docusaurus project. You can name it modal.md. If a file for the modal documentation already exists, open it.

Write the Documentation:
Use the following template to create a detailed documentation for your modal component.

Here's an example modal.md file:

markdown

---
id: modal
title: Modal Component
sidebar_label: Modal
---

## Overview

The Modal component is used to display content in a layer above the main content. It can be used for dialogs, lightboxes, and other temporary content.

## Installation

To use the Modal component, install the library:

```bash
npm install your-modal-library

Basic Usage

import React, { useState } from 'react';
import Modal from 'your-modal-library';

function App() {
  const [isOpen, setIsOpen] = useState(false);

  return (
    <div>
      <button onClick={() => setIsOpen(true)}>Open Modal</button>
      <Modal isOpen={isOpen} onClose={() => setIsOpen(false)}>
        <h2>Modal Title</h2>
        <p>Modal Content</p>
        <button onClick={() => setIsOpen(false)}>Close Modal</button>
      </Modal>
    </div>
  );
}
Props
The Modal component accepts the following props:

Prop	Type	Default	Description
isOpen	boolean	false	Whether the modal is open or not.
onClose	function	undefined	Function to call when the modal is closed.
title	string	undefined	Title of the modal.
children	node	undefined	Content of the modal.
Variants
Examples of different modal variants:

import Modal from 'your-modal-library';

// Info Modal
<Modal isOpen={isOpen} onClose={handleClose} variant="info">
  <h2>Info Modal</h2>
  <p>This is an info modal.</p>
</Modal>

// Warning Modal
<Modal isOpen={isOpen} onClose={handleClose} variant="warning">
  <h2>Warning Modal</h2>
  <p>This is a warning modal.</p>
</Modal>

// Error Modal
<Modal isOpen={isOpen} onClose={handleClose} variant="error">
  <h2>Error Modal</h2>
  <p>This is an error modal.</p>
</Modal>
Custom Styles
To apply custom styles to the modal:

import './custom-modal.css';

<Modal isOpen={isOpen} onClose={handleClose} className="custom-modal">
  <h2>Custom Styled Modal</h2>
  <p>This modal has custom styles.</p>
</Modal>
Accessibility
The Modal component supports ARIA attributes to improve accessibility. For example:

<Modal isOpen={isOpen} onClose={handleClose} aria-labelledby="modal-title" aria-describedby="modal-description">
  <h2 id="modal-title">Accessible Modal</h2>
  <p id="modal-description">This modal is accessible.</p>
</Modal>
Examples
Comprehensive examples showing the modal in various contexts:

import React, { useState } from 'react';
import Modal from 'your-modal-library';

function Example() {
  const [isModalOpen, setIsModalOpen] = useState(false);

  return (
    <div>
      <button onClick={() => setIsModalOpen(true)}>Show Modal</button>
      <Modal isOpen={isModalOpen} onClose={() => setIsModalOpen(false)}>
        <h2>Example Modal</h2>
        <p>This is an example modal.</p>
        <button onClick={() => setIsModalOpen(false)}>Close</button>
      </Modal>
    </div>
  );
}
#Troubleshooting
Common issues and solutions related to the modal component:

Modal not opening/closing: Ensure that the isOpen prop is properly passed and toggled.
Modal styles not applying: Verify that the correct CSS classes are being used and that there are no conflicts with other styles.

#API Reference
The Modal component provides the following methods and events:

open(): Opens the modal.
close(): Closes the modal.
onClose: Event triggered when the modal is closed.


3. **Update Sidebar Configuration:**
   If you haven't already, include the new documentation page in the sidebar. Update the `sidebars.js` file in the `sidebars` directory. Add an entry for your new modal documentation page.

   Example `sidebars.js`:

   ```js
   module.exports = {
     docs: [
       {
         type: 'category',
         label: 'Components',
         items: ['button', 'modal'], // Add 'modal' to the items array
       },
       // other categories or items
     ],
   };

````
