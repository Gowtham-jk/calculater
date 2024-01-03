# Design of a Standard Calculator

## AIM:

To design a web application for a standard calculator.

## DESIGN STEPS:

### Step 1:
 Fork the github repository at https://github.com/gowriganeshns/standard-calculator

### Step 2:
 cd standard-calculator and then create a django project by typing:

 django-admin startproject myproj


### Step 3:
 go to settings.py under myproj/myproj and make the following changes

 1) in line 14, add import os

 2) under ALLOWED_HOSTS, include '*' in the list.

 3) at the end, in line 121, add the following code:
    
    STATICFILES_DIRS = [
        os.path.join(BASE_DIR,'static')
    ]


### Step 4:
 Now that we have made the changes, type the following commands to create a folder static, and then another folder html in it.

 (from standard-calculator/myproj)

 mkdir static
 cd static
 mkdir html
 cd html

### Step 5:
 create a html file under html folder

 touch calc.html

 now, add your code in the html file.

### Step 6:

Validate the HTML and CSS code.

### Step 6:

Publish the website in the given URL.

## PROGRAM :
```
calc.html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="/static/CSS/style.css">
    <title>Calculator</title>
</head>
<body>
    <div class="container">
        <h1>GOWTHAM's Calculator</h1>

        <div class="calculator">
            <input type="text" name="screen" id="screen">
            <table>
                <tr>
                    <td><button>(</button></td>
                    <td><button>)</button></td>
                    <td><button>C</button></td>
                    <td><button>%</button></td>
                </tr>
                <tr>
                    <td><button>7</button></td>
                    <td><button>8</button></td>
                    <td><button>9</button></td>
                    <td><button>X</button></td>
                </tr>
                <tr>
                    <td><button>4</button></td>
                    <td><button>5</button></td>
                    <td><button>6</button></td>
                    <td><button>-</button></td>
                </tr>
                <tr>
                    <td><button>1</button></td>
                    <td><button>2</button></td>
                    <td><button>3</button></td>
                    <td><button>+</button></td>
                </tr>
                <tr>
                    <td><button>0</button></td>
                    <td><button>.</button></td>
                    <td><button>/</button></td>
                    <td><button>=</button></td>
                </tr>
            </table>
        </div>
    </div>

</body>
<script src="/static/JS/index.js"></script>
</html>

index.js

let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }

    })
}

style.css

.container{
    text-align: center;
    margin-top:23px
}

table{
    margin: auto;
}

input{
    border-radius: 21px;
    border: 5px solid #244624;
    font-size:34px;
    height: 65px;
    width: 456px;
}

button{
    border-radius: 20px;
    font-size: 40px;
    background: #978fa0;
    width: 102px;
    height: 90px;
    margin: 6px;
}

.calculator{ 
    border: 4px solid #13695d;
    background-color: red;
    padding: 23px;
    border-radius: 53px;
    display: inline-block;
    
}

h1{
    font-size: 28px;
    font-family: 'Courier New', Courier, monospace;
}

```

 ## OUTPUT:

![cal1](https://github.com/Gowtham-jk/calculater/assets/149857834/7e2d6891-4e9a-4175-a742-493485cd56a3)
![cal2](https://github.com/Gowtham-jk/calculater/assets/149857834/8bd8db40-4f08-4a95-a4f5-1ad1d27c708d)


## Result:

THE PROGRAM WAS EXECUTED SUCCESSFULLY.
