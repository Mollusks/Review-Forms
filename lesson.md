## 1. The Form Shell (The Container)
*   **The Basic Structure:** All forms must be contained within a pair of `<form>` tags [1].
*   **The Action Attribute:** This defines the destination where the data is sent, such as a URL or a dynamic programming page like PHP [2].
*   **The Method Attribute:** This determines how the data is transmitted [2]:
    *   **GET:** Appends data to the URL (visible and insecure); best for search boxes [2, 3].
    *   **POST:** Submits data securely without displaying it in the URL; best for passwords and sensitive information [2, 3].
*   **Closing the Shell:** The `</form>` tag should only be entered after the submit button is in place.

## 2. Labels and Accessibility
*   **The Label:** Acts as the "question" for the user so they know what information to enter [1].
*   **Accessibility:** It is good practice to use the `for` attribute in a label and set it to match the input's `id` [1].
*   **Functionality:** Clicking a linked label will automatically select the associated input box, which also helps people using screen readers navigate the form [1, 4].

## 3. Core Input Types
*   **Text & Password:** Use `type="text"` for general input and `type="password"` to hide characters [1, 5].
*   **Email:** `type="email"` requires the user to include an "@" character for a valid submission [5].
*   **Date:** `type="date"` provides an interactive calendar for selecting dates [5].
*   **Number:** `type="number"` allows numeric entry and can include `min`, `max`, and a default `value` [5, 6].
*   **Buttons:** `type="submit"` sends the data to the action destination, while `type="reset"` clears all current inputs [2].

## 4. Key Data Attributes
*   **The Name Attribute:** This acts like a "variable" or a unique key for the data when it is collected on the server [2, 4].
*   **Placeholder:** Provides default hint text (e.g., "Spongebob") that disappears when the user starts typing [4].
*   **Required:** This boolean attribute prevents the form from being submitted if the field is empty, often triggering a browser pop-up [3].
*   **Maxlength:** Limits the number of characters a user can type into a field, such as a password [5].

## 5. Selection and Choice
*   **Radio Buttons:** Used for multiple-choice questions where only one answer can be selected [6]. 
*   **Radio Grouping:** To ensure only one radio button can be selected, give every option in that group the **same matching name** [6].
*   **Dropdown Menus:** Created using `<select>` tags with individual `<option>` tags inside; each option requires a `value` attribute to define what data is sent [7, 8].
*   **Checkboxes:** Used for simple binary choices, such as a "Subscribe" button [8].

## 6. Layout and Organization
*   **Fieldset & Legend:** Use a `<fieldset>` to draw a visual border around the form and a `<legend>` to give that section a title.
*   **Textarea:** Acts like a "paragraph" input for longer, multi-line text requests.
*   **Spacing:** To prevent labels and inputs from appearing on the same line, wrap each pair in a `<div>` element or use line breaks to treat them as block-level elements [2, 4].


Examples
--------------------------------------------------------------------------------
Here is an example:

```html
<form action="/submit-reservation" method="POST">
  <h2>Reservation Form</h2>

  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required /><br>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required /><br>

  <label for="phone">Phone:</label>
  <input type="tel" id="phone" name="phone" required /><br>

  <label for="date">Date:</label>
  <input type="date" id="date" name="date" required /><br>

  <label for="party-size">Party Size:</label>
  <input type="number" id="party-size" name="party-size" min="1" required /><br>

  <label for="requests">Special Requests:</label><br>
  <textarea id="requests" name="requests" rows="4" placeholder="Let us know if you have any special needs..."></textarea><br>

  <button type="submit">Submit Reservation</button>
</form>
```

Walkthrough
--------------------------------------------------------------------------------
1. Make a simple name form using what you learned in Form Shell
Example:
```html
<form method="POST">
  <label>Name:</label>
  <input type="text" id="name" name="name" />
</form>
```

2. Make a new form, make it about email and phone-number
Example:
```html
<form method="POST">
  <label>Email:</label>
  <input type="email" id="email" name="email" />
    <label>Telephone:</label>
  <input type="tel" id="tele" name="tele" />
</form>
```

3. Make a full form with name, emial, phone number, and all form questions required
```html
<form method="POST">
  <label>Name:</label>
    <input type="text" id="name" name="name" required/>
  <label>Email:</label>
    <input type="email" id="email" name="email" required/>
  <label>Telephone:</label>
    <input type="tel" id="tele" name="tele" required/>
</form>
```

Video Link: [https://www.youtube.com/playlist?list=PL3md42W5AI8-IyFErdGsdnX5O4i_sCTi0&jct=J87udO4Fx7jUSLOORDVIIA](https://www.youtube.com/watch?v=2O8pkybH6po)

Things to remember
--------------------------------------------------------------------------------
1. Correct Formatting
2. Correct spelling
3. Using label to label the form questions
4. Using the correct input type

5. Make sure to use required when needed

