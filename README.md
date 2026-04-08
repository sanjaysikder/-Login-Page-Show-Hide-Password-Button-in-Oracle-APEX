# 🔐 Login Page Show / Hide Password Button in Oracle APEX

This guide explains how to add a **Show/Hide Password toggle button** in an Oracle APEX password field using HTML, JavaScript, and CSS.

---

## 📌 Step 1: Add Button to Password Item

Go to your **Password Item → Post Text** and add:

```html
<button type="button" onclick="viewPWD()"  style="height:40px; border:1px solid #87ceeb !important;">     
    <span id="pwdItem" class="fa fa-eye pw-item-icon"></span>  
</button>

```
## 📌 Step 2: Add JavaScript Function

- Navigate to:

- Page Designer → Page → Function and Global Variable Declaration

```Add the following javaScript code:

function viewPWD()
{
    var Vpw = document.getElementById('P9999_PASSWORD');
    var VsetIcon = document.getElementById('pwdItem');
 
    if (Vpw.type != 'password'){
         Vpw.type='password';
         VsetIcon.className='fa fa-eye pw-item-icon';
    }
    else
    {
        Vpw.type='text';
        VsetIcon.className='fa fa-eye-slash pw-item-icon';
    }
}

```
## 📌 Step 3: Add CSS Styling

- Go to:

- Page → Inline CSS

```Add the following css:

/* Style the toggle button inside the input field */
.pwd-toggle {
    position: absolute;
    right: 0;
    top: 0;
    height: 100%;
    width: 45px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    
    background: #f4f4f4;
    border-left: 1px solid #d0d0d0;
    border-radius: 0 4px 4px 0;
    
    z-index: 5;
}

```

## ✅ Final Result

- 👁️ Click → Show password  
- 🙈 Click again → Hide password  
- Button stays inside the password field  
- No page submit on click  


 # Thank you
 ## Sanjay Sikder

 You can connect with me on [LinkedIn](https://www.linkedin.com/in/sanjay-sikder/)!
