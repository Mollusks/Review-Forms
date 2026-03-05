Form Shell
--------------------------------------------------------------------------------
Before starting to make a form, you must make the shell. By using ```<form> </form>``` you can then insert things into that. A form is used to input data for collection, such as a quiz or test. You cannot make a form without the shell. The ending argument ```</form>``` should only be entered once you have your submit button at the end already. Action allows you to pick the destination, in most cases where you don't have a server, it would be the URl. Method is used to either send or recieve information from the URL or server.

Labeling and Inputs
--------------------------------------------------------------------------------
Label: Before an input, you must label it so the users know what to put in tha field. The labeling works as a question.

Inputs: Inputs are things that are inputted. There are a few key types of input types: Text, email, date, select, checkbox, radio, range, and submit. A Text input type is just plain text, an email input type expects an @address.com/org, a date input type is for selecting dates, a checkbox is a checkbox, the radio input type is a multiple choice question where you can only select one answer, range input type allows you to enter a range, Select is a dropdown multilechoice question, and the submit type allows you to submit the form. To correctly insert an input you must enter ```<input type="" name="" />```. Inputs can be required, meaning they must answer before it lets them submit. To make it required you enter required at the end: ```<input type="" name="" required />```

Attributes
--------------------------------------------------------------------------------
The name attribute acts like an ID when the data is collected. When the data is collected the name will show as the unique key/name for that single input/question. For certain number based inputs you can insert a minimum and/or a maximum. For a placeholder text, which is text that is used to show when something is text, you can use ```placeholder=""``` in a ```<textarea></textarea>```, a text area is most like a paragraph input, allowing you you to write in a box as a request. The legend acts as a name for the form., the fieldset encompasses the entire form to add a line around it. ```value=""``` is used for what the value id actually is for a select/dropdown.

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
