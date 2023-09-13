# Information-Card

This is a simple HTML, CSS, and JavaScript code that creates an information card that displays a user's first name, last name, country, phone number, state, city, and village.

## How to use

1. The repository is cloned.

2. index.html file is opened in the text editor.

3. The user should fill their information in the fields.

4. The file is saved.

5. Open the index.html in the web browser.

**Step-1**:**Creation of HTML File**

A HTML file is created and the following code is added:

```

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Information Card</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="main-container">
        <div class="infoCard">
            <h1>User Info Card</h1>
            <div class="userInfo">
                <div class="field">
                    <span class="label">First Name:</span>
                    <span id="firstName"></span>
                </div>

                <div class="field">
                    <span class="label">Last Name:</span>
                    <span id="lastName"></span>
                </div>

                <div class="field">
                    <span class="label">Country:</span>
                    <span id="country"></span>
                </div>

                <div class="field">
                    <span class="label">Phone Number:</span>
                    <span id="phoneNumber"></span>
                </div>

                <div class="field">
                    <span class="label">State:</span>
                    <span id="state"></span>
                </div>

                <div class="field">
                    <span class="label">City:</span>
                    <span id="city"></span>
                </div>

                <div class="field">
                    <span class="label">Village:</span>
                    <span id="village"></span>
                </div>

             </div>

 ```

**Step-2**:**Creation of CSS File**

A Css File is created and the following code is added in the file:

```

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body{
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: rgb(7, 8, 8);
}

.main-container {
  background-color: #f8fcff;
  border-radius: 10px;
  box-shadow: rgb(163, 97, 228) 1px 3px 9px;
  padding: 20px;
  max-width: 400px;
  width: 100%;
}

h1{
  font-size: 24px;
  color: #e70a0a;
  margin-bottom: 20px;
  text-align: center;
  font-weight: 600;
  font-family: cursive;
  border-bottom: 3px outset rgb(217, 62, 217);
}

h1:hover{
  color: rgb(241, 15, 166);
  scale: 0.9;
}


.field {
  display: flex;
  justify-content: space-between;
  margin-bottom: 10px;
  font-weight: 400;
}

.label {
  font-weight: 500;
  color: #f83535;
  flex: 1;
}

.userInfo span {
  flex: 2;
  color: #f53d0a;
  text-align: left;
  padding-left: 10px;
}

.infoCard {
  text-align: center;
}

```

**Step-3**:**Creation of JS File**

A JS File is created and the following code is added:

```

const storedUserInfo = localStorage.getItem("userInfo");
if (storedUserInfo) {
  const userInfo = JSON.parse(storedUserInfo);
  document.getElementById("firstName").textContent = userInfo.firstName;
  document.getElementById("lastName").textContent = userInfo.lastName;
  document.getElementById("country").textContent = userInfo.country;
  document.getElementById("phoneNumber").textContent = userInfo.phoneNumber;
  document.getElementById("state").textContent = userInfo.state;
  document.getElementById("city").textContent = userInfo.city;
  document.getElementById("village").textContent = userInfo.village;
}
function storeUserInfo() {
  const firstName = prompt("Enter your first name:");
  const lastName = prompt("Enter your last name:");
  const country = prompt("Enter your country:");
  const phoneNumber = prompt("Enter your phone number:");
  const state = prompt("Enter your state:");
  const city = prompt("Enter your city:");
  const village = prompt("Enter your village:");

  const userInfo = {
    firstName,
    lastName,
    country,
    phoneNumber,
    state,
    city,
    village,
  };

  localStorage.setItem("userInformation", JSON.stringify(userInfo));
  document.getElementById("firstName").textContent = userInfo.firstName;
  document.getElementById("lastName").textContent = userInfo.lastName;
  document.getElementById("country").textContent = userInfo.country;
  document.getElementById("phoneNumber").textContent = userInfo.phoneNumber;
  document.getElementById("state").textContent = userInfo.state;
  document.getElementById("city").textContent = userInfo.city;
  document.getElementById("village").textContent = userInfo.village;
}
storeUserInfo();

```
## Explanation of Code 

Here in this project the HTML code gives the basic structure to the Information Card.The Css code has the role for making the card more stylsh and JS code populates the card with the user's information.

The HTML code contains an element with the ID of infoCard. This element contains all of the other elements on the card.

The CSS code styles the info-card element with a width of 300px, a height of 200px, and a background color of rgb(7, 8, 8). The CSS code also styles the text on the card with a font size of 16px.

The JavaScript code gets the user's information from the fields in the HTML code. The JavaScript code then populates the card with the user's information.





          

