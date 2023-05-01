
# Login & Registration Page

This project shows an understanding of Html, CSS, and JS. In this project, we created a login page where the user is going to interact with and create their account. If the user doesn't have an account then they must register and create the account that way. When the user presses the Login in the top right then the Login page shows up. When the user presses the close icon in red then the login page closes. 
## Project Preview

![QR_Code_Design](https://github.com/zaidaslam99/login_register_website/blob/main/project_screenshots/login_shot.png?raw=true)

![QR_Code_Design](https://github.com/zaidaslam99/login_register_website/blob/main/project_screenshots/register_shot.png?raw=true)

## Code Snippet

### HTML
```html
<div class="wrapper">
    
    <!-- Close Icon to close the login page -->
    <span class="icon-close"><ion-icon name="close-outline"></ion-icon></span>

    <div class="form-box login">
    <h2>Login</h2>
    <form action="#">
        <div class="input-box">
        <span class="icon"><ion-icon name="mail-outline"></ion-icon></span>
        <input type="email" required />
        <label>Email</label>
        </div>
        <div class="input-box">
        <span class="icon"
            ><ion-icon name="lock-closed-outline"></ion-icon
        ></span>
        <input type="password" required />
        <label>Password</label>
        </div>
        <div class="remember-forgot">
        <label><input type="checkbox" /> Remember Me</label>
        <a href="#">Forgot Password?</a>
        </div>
        <button type="submit" class="btn">Login</button>
        <div class="login-register">
        <p>
            Don't have an account?<a href="#" class="register-link"> Register</a></a
            >
        </p>
        </div>
    </form>
    </div>

    <div class="form-box register">
    <h2>Registration</h2>
    <form action="#">
        <div class="input-box">
        <span class="icon"><ion-icon name="person-outline"></ion-icon></span>
        <input type="text" required />
        <label>Username</label>
        </div>
        
        <div class="input-box">
        <span class="icon"><ion-icon name="mail-outline"></ion-icon></span>
        <input type="email" required />
        <label>Email</label>
        </div>
        <div class="input-box">
        <span class="icon"
            ><ion-icon name="lock-closed-outline"></ion-icon
        ></span>
        <input type="password" required />
        <label>Password</label>
        </div>
        <div class="remember-forgot">
        <label><input type="checkbox" /> I agree to terms & conditions</label>
        </div>
        <button type="submit" class="btn">Register</button>
        <div class="login-register">
        <p>
            Already have an account?<a href="#" class="login-link"> Login</a></a
            >
        </p>
        </div>
    </form>
    </div>

</div>
```

### JavaScript

```js
const wrapper = document.querySelector(".wrapper");
const loginLink = document.querySelector(".login-link");
const registerLink = document.querySelector(".register-link");
const btnPopup = document.querySelector(".btnLogin-popup");
const iconClose = document.querySelector(".icon-close");

registerLink.addEventListener("click", () => {
  wrapper.classList.add("active");
});

loginLink.addEventListener("click", () => {
  wrapper.classList.remove("active");
});

btnPopup.addEventListener("click", () => {
  wrapper.classList.add("active-popup");
});

iconClose.addEventListener("click", () => {
  wrapper.classList.remove("active-popup");
});
```

## Lessons Learned

### HTML

So the important thing to understand here is that we have an outer div and this has a class called .wrapper within it we are going to be having two div containers one container is going to be for the form-box login and the other container is going to be for the form-box register. The Login form is only going to be taking the username and the password as suppose to the registration form which is going to be taking the username, email, and password. 
 
### JavaScript

So addEventListener makes adding many events handlers to one element easy, it lets you respond to events associated with an element by an event handler function. Notice what we did we are using querySelector and choosing the appropriate node once we have those nodes stored to a variable we then are running an addEventListener on them. The addEventListener is going to be hearing for click and within it notice we are using classList and then their respective methods. What we are doing here is the tags that we stored to the variables we are essentially adding classes to them to get the respected outcomes that we want.