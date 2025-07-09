# Saveetha_Admission_clone
## Date: 09/07/2025

## Objective:
To design a landing page clone of Saveetha Engineering College’s Admission Enquiry form using HTML and CSS. This activity reinforces skills in layout design, form creation, user input handling, responsive structure, and visual styling based on a real-world example.

## Tasks:
#### 1. Analyze the Landing Page Layout:
Observe the split-screen layout with a promotional section on the left and a form on the right.

Note the use of background images, text styling, and branding elements.

#### 2. Create the HTML Structure:
Use semantic tags like ```<section>, <header>, <form>, and <footer>``` to organize content.

Structure the form with input fields such as name, email, phone, password, city, state, course, specialization, captcha, and checkbox.

#### 3. Add Form Functionality:
Include appropriate input types (text, email, tel, password, select, etc.) with placeholders and labels.

Use the <button> element for the "APPLY NOW" action.

#### 4. Apply CSS Styling:
Implement a split layout using flexbox or grid.

Style the form elements with padding, shadows, background colors, and rounded borders.

Include hover effects and button transitions to match the original look.

#### 5. Incorporate Images and Branding:
Add the institution logo and use matching fonts and colors.

Place a background image or blurred overlay behind the form content if needed.

#### 6. Ensure Responsiveness:
Make sure the page adapts to different screen sizes using media queries.

Maintain readability and layout integrity on both desktop and mobile.

## HTML Code:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <section id="background">
        <img src="image.jpg" alt="saveetha_banner_image" class="image">
        <div class="form-container">
            <h2>Admissions Open 2025</h2>

            <form>
                <input type="text" placeholder="Enter Name *">
                <input type="text" placeholder="Enter Email Address *">

                <div class="phone-container">
                    <select>
                        <option selected="True">+91</option>
                        <option>India(+91)</option>
                        <option>Afganistan(+93)</option>
                        <option>Albania(+355)</option>
                        <option>Algeria(+213)</option>
                    </select>
                    <input type="number" placeholder="Enter Mobile Number">
                </div>

                <input type="password" placeholder="Any Password of Your Choice">

                <div class="info-container">
                    <div class="container">
                        <select>
                            <option selected="True">State *</option>
                        <option value="">TamilNadu</option>
                        <option value="">Andhra Pradhesh</option>
                        <option value="">Delhi</option>
                        <option value="">Karnataka</option>
                    </select>
                    <select name="" id="">
                        <option selected="True">City *</option>
                        <option value="">Chennai</option>
                        <option value="">Hyderabad</option>
                        <option value="">Agra</option>
                        <option value="">Banglore</option>
                    </select>
                    </div>
                    
                    <div class="container">
                        <select name="" id="">
                            <option selected="True">Course *</option>
                        <option value="">B.Tech or B.E</option>
                        <option value="">Lateral Entry</option>
                        <option value="">M.E</option>
                        <option value="">MBA</option>
                    </select>
                    <select name="" id="">
                        <option selected="True">Specialization *</option>
                        <option value="">CSE</option>
                        <option value="">IT</option>
                        <option value="">ECE</option>
                        <option value="">IOT</option>
                    </select>
                    </div>
                </div>

                <div class="acknowledge">
                    <input type="checkbox">
                    <p> authorise Saveetha Engineering College & its representatives to contact me with updates and notifications via Email/SMS/What'sApp/Call. This will override DND/NDNC *</p>
                </div>

                <button type="submit">Apply Now</button>
            </form>

            <h3>Already have an Account ? <a href="">Login</a></h3>
            <h3><a href="">Send Verification Email</a></h3>
        </div>
    </section>
</body>
</html>
```

## CSS Code:
```
body{
    margin: 0;
    font-family:'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

h2, p{
    color: white;
}

h3{
    color: white;
    margin-top: 0;
    margin-bottom: 0;
}

a{
    text-decoration: none;
    color: white;
}

a:hover{
    text-decoration: underline;
}

.image{
    margin-top: 0;
    width: 100%;
    height: 100vh;
}

.background{
    position: relative;
}

.form-container {
    position: absolute;
    top: 10%;
    left: 65%;
    background-color: rgba(0, 0, 0, 0.5); /* white with 80% opacity */
    width: 22%;
    text-align: center;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 4px 20px rgba(0, 0, 0, 1);
}


form{
    display: flex;
    flex-direction: column;
    padding: 0 4% 4% 4%;
}

.phone-container{
    display: flex;
    flex-direction: row;
    width: 100%;
    justify-content: space-between;
}

.phone-container select{
    width: 30%;

}

.phone-container input{
    width: 60%;
}

.info-container{
    display: flex;
    flex-direction: column;
    margin-bottom: 10px;
}   

.container{
    width: 100%;
    display: flex;
    justify-content: space-between;
}

select{
    width: 40%;;
}

.acknowledge {
    position: relative;
    padding-left: 25px;
}

.acknowledge input[type="checkbox"] {
    position: absolute;
    top: 0;
    left: 0;
}

.acknowledge p {
    margin: 0;
    text-align: justify;
}

input{
    padding: 10px;
    margin-bottom: 5px;
}

select{
    padding: 10px;
    margin-bottom: 5px;
    width: 49%;
}

button{
    margin-top: 10px;
    padding: 10px;
    background-color: #D79E2F;
    border: none;
}

button:hover{
    background-color: white;
    color:#D79E2F
}



/* media query for mobile devices */
@media (max-width: 768px) {
  .form-container {
    position: static;
    width: 80%;
    margin: 20px auto;
    box-shadow: none;
    border-radius: 5px;
    background-color: rgb(79, 88, 79);
  }

  .image{
    width: 100%;
    height: 200px;
  }

  form {
    padding: 0;
  }

  .phone-container {
    flex-direction: row;
  }

  .phone-container select{
    margin-bottom: 10px;
    width: 30%;
    margin-right: 5px;
  }
  .phone-container input {
    width: 100%;
    margin-bottom: 10px;
  }

  .container {
    flex-direction: column;
  }

  .container select {
    width: 100%;
    margin-bottom: 10px;
  }

  select {
    width: 100%;
  }

  .acknowledge {
    font-size: 13px;
  }

  button {
    width: 100%;
  }
}
```

## Output:
## Desktop : 
![image](https://github.com/user-attachments/assets/0d7a2833-07fd-47ff-8060-2096f33ca975)

## Mobile : 
![image](https://github.com/user-attachments/assets/00f3e2e6-1613-40a8-9ee5-dda4ba09c3e3)

## Result:
A landing page clone of Saveetha Engineering College’s Admission Enquiry form using HTML and CSS is designed successfully.
