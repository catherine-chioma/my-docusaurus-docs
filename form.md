---
id: form
title: Form Component
sidebar_label: Form
---

## Overview

The Form component is used to collect and validate user inputs. It can include various form elements such as inputs, checkboxes, radio buttons, and more.

## Installation

To use the Form component, install the library:

````bash
npm install your-form-library

Basic Usage
Here’s a basic example of using the Form component:

import React, { useState } from 'react';
import Form from 'your-form-library';

function App() {
  const [formData, setFormData] = useState({
    name: '',
    email: ''
  });

  const handleChange = (e) => {
    const { name, value } = e.target;
    setFormData({
      ...formData,
      [name]: value
    });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    alert(`Name: ${formData.name}, Email: ${formData.email}`);
  };

  return (
    <Form onSubmit={handleSubmit}>
      <label>
        Name:
        <input type="text" name="name" value={formData.name} onChange={handleChange} />
      </label>
      <label>
        Email:
        <input type="email" name="email" value={formData.email} onChange={handleChange} />
      </label>
      <button type="submit">Submit</button>
    </Form>
  );
}


#Props
The Form component accepts the following props:

Prop	Type	Default	Description
onSubmit	function	undefined	Function to call when the form is submitted.
children	node	undefined	Content of the form, usually form elements.
className	string	undefined	Additional class names to apply to the form.

#Custom Styles
To apply custom styles to the form:

import './custom-form.css';

<Form onSubmit={handleSubmit} className="custom-form">
  <label>
    Name:
    <input type="text" name="name" value={formData.name} onChange={handleChange} />
  </label>
  <label>
    Email:
    <input type="email" name="email" value={formData.email} onChange={handleChange} />
  </label>
  <button type="submit">Submit</button>
</Form>


Validation
An example of a form with validation:

import React, { useState } from 'react';
import Form from 'your-form-library';

function App() {
  const [formData, setFormData] = useState({
    name: '',
    email: ''
  });
  const [errors, setErrors] = useState({});

  const handleChange = (e) => {
    const { name, value } = e.target;
    setFormData({
      ...formData,
      [name]: value
    });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    let formErrors = {};
    if (!formData.name) {
      formErrors.name = 'Name is required';
    }
    if (!formData.email) {
      formErrors.email = 'Email is required';
    }
    setErrors(formErrors);
    if (Object.keys(formErrors).length === 0) {
      alert(`Name: ${formData.name}, Email: ${formData.email}`);
    }
  };

  return (
    <Form onSubmit={handleSubmit}>
      <label>
        Name:
        <input type="text" name="name" value={formData.name} onChange={handleChange} />
        {errors.name && <span className="error">{errors.name}</span>}
      </label>
      <label>
        Email:
        <input type="email" name="email" value={formData.email} onChange={handleChange} />
        {errors.email && <span className="error">{errors.email}</span>}
      </label>
      <button type="submit">Submit</button>
    </Form>
  );
}


Accessibility
The Form component supports ARIA attributes to improve accessibility. For example:

<Form onSubmit={handleSubmit} aria-labelledby="form-title">
  <h2 id="form-title">Accessible Form</h2>
  <label>
    Name:
    <input type="text" name="name" value={formData.name} onChange={handleChange} aria-required="true" />
  </label>
  <label>
    Email:
    <input type="email" name="email" value={formData.email} onChange={handleChange} aria-required="true" />
  </label>
  <button type="submit">Submit</button>
</Form>



To write documentation for a form component using Docusaurus, you'll follow a similar process as with other components. This involves creating a detailed markdown file that describes the form's usage, props, examples, and other relevant information.

Here’s a step-by-step guide:

Create or Open a Documentation File:
If you haven't already, create a new markdown file in the docs directory of your Docusaurus project. You can name it form.md. If a file for the form documentation already exists, open it.

Write the Documentation:
Use the following template to create a detailed documentation for your form component.

Here's an example form.md file:

markdown
Copy code
---
id: form
title: Form Component
sidebar_label: Form
---

## Overview

The Form component is used to collect and validate user inputs. It can include various form elements such as inputs, checkboxes, radio buttons, and more.

## Installation

To use the Form component, install the library:

```bash
npm install your-form-library
or

bash
Copy code
yarn add your-form-library
Basic Usage
Here’s a basic example of using the Form component:

jsx
Copy code
import React, { useState } from 'react';
import Form from 'your-form-library';

function App() {
  const [formData, setFormData] = useState({
    name: '',
    email: ''
  });

  const handleChange = (e) => {
    const { name, value } = e.target;
    setFormData({
      ...formData,
      [name]: value
    });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    alert(`Name: ${formData.name}, Email: ${formData.email}`);
  };

  return (
    <Form onSubmit={handleSubmit}>
      <label>
        Name:
        <input type="text" name="name" value={formData.name} onChange={handleChange} />
      </label>
      <label>
        Email:
        <input type="email" name="email" value={formData.email} onChange={handleChange} />
      </label>
      <button type="submit">Submit</button>
    </Form>
  );
}
Props
The Form component accepts the following props:

Prop	Type	Default	Description
onSubmit	function	undefined	Function to call when the form is submitted.
children	node	undefined	Content of the form, usually form elements.
className	string	undefined	Additional class names to apply to the form.
Custom Styles
To apply custom styles to the form:

jsx
Copy code
import './custom-form.css';

<Form onSubmit={handleSubmit} className="custom-form">
  <label>
    Name:
    <input type="text" name="name" value={formData.name} onChange={handleChange} />
  </label>
  <label>
    Email:
    <input type="email" name="email" value={formData.email} onChange={handleChange} />
  </label>
  <button type="submit">Submit</button>
</Form>
Validation
An example of a form with validation:

jsx
Copy code
import React, { useState } from 'react';
import Form from 'your-form-library';

function App() {
  const [formData, setFormData] = useState({
    name: '',
    email: ''
  });
  const [errors, setErrors] = useState({});

  const handleChange = (e) => {
    const { name, value } = e.target;
    setFormData({
      ...formData,
      [name]: value
    });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    let formErrors = {};
    if (!formData.name) {
      formErrors.name = 'Name is required';
    }
    if (!formData.email) {
      formErrors.email = 'Email is required';
    }
    setErrors(formErrors);
    if (Object.keys(formErrors).length === 0) {
      alert(`Name: ${formData.name}, Email: ${formData.email}`);
    }
  };

  return (
    <Form onSubmit={handleSubmit}>
      <label>
        Name:
        <input type="text" name="name" value={formData.name} onChange={handleChange} />
        {errors.name && <span className="error">{errors.name}</span>}
      </label>
      <label>
        Email:
        <input type="email" name="email" value={formData.email} onChange={handleChange} />
        {errors.email && <span className="error">{errors.email}</span>}
      </label>
      <button type="submit">Submit</button>
    </Form>
  );
}
Accessibility
The Form component supports ARIA attributes to improve accessibility. For example:

jsx
Copy code
<Form onSubmit={handleSubmit} aria-labelledby="form-title">
  <h2 id="form-title">Accessible Form</h2>
  <label>
    Name:
    <input type="text" name="name" value={formData.name} onChange={handleChange} aria-required="true" />
  </label>
  <label>
    Email:
    <input type="email" name="email" value={formData.email} onChange={handleChange} aria-required="true" />
  </label>
  <button type="submit">Submit</button>
</Form>

#Examples
Comprehensive examples showing the form in various contexts:

import React, { useState } from 'react';
import Form from 'your-form-library';

function Example() {
  const [formData, setFormData] = useState({
    name: '',
    email: ''
  });

  const handleChange = (e) => {
    const { name, value } = e.target;
    setFormData({
      ...formData,
      [name]: value
    });
  };

  const handleSubmit = (e) => {
    e.preventDefault();
    alert(`Name: ${formData.name}, Email: ${formData.email}`);
  };

  return (
    <Form onSubmit={handleSubmit}>
      <label>
        Name:
        <input type="text" name="name" value={formData.name} onChange={handleChange} />
      </label>
      <label>
        Email:
        <input type="email" name="email" value={formData.email} onChange={handleChange} />
      </label>
      <button type="submit">Submit</button>
    </Form>
  );
}

#Troubleshooting
Common issues and solutions related to the form component:

Form not submitting: Ensure that the onSubmit prop is properly passed and that the form has a submit button.
Form styles not applying: Verify that the correct CSS classes are being used and that there are no conflicts with other styles.
Validation errors: Ensure that validation logic is correctly implemented and that error messages are displayed properly.

API Reference
The Form component provides the following methods and events:

reset(): Resets the form fields.
submit(): Submits the form programmatically.
onSubmit: Event triggered when the form is submitted.


3. **Update Sidebar Configuration:**
   Include the new documentation page in the sidebar. Update the `sidebars.js` file in the `sidebars` directory. Add an entry for your new form documentation page.

   Example `sidebars.js`:

   ```js
   module.exports = {
     docs: [
       {
         type: 'category',
         label: 'Components',
         items: ['button', 'modal', 'form'], // Add 'form' to the items array
       },
       // other categories or items
     ],
   };


````
