# Ex.05 Design a Website for Server Side Processing
## Date:24.09.2025

## AIM:
 To design a website to calculate the power of a lamp filament in an incandescent bulb in the server side. 


## FORMULA:
bmi=w/h<sup2></sup>
<br>w-->weight(in kg)
<br>h-->height (in cm)

## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Create python programs for views and urls to perform server side processing.

### Step 5:
Create a HTML file to implement form based input and output.

### Step 6:
Publish the website in the given URL.

## PROGRAM :
```
from django.shortcuts import render

def calculate_bmi(request):
    bmi = None

    if request.method == "POST":
        try:
            height_cm = float(request.POST.get("height"))
            weight_kg = float(request.POST.get("weight"))
            height_m = height_cm / 100  # convert cm to meters
            
            bmi = weight_kg / (height_m * height_m)

            print(f"Calculated BMI: {bmi:.2f}")  # Output to console

        except (TypeError, ValueError, ZeroDivisionError):
            bmi = None

    return render(request, "bmiapp/template.html", {"BMI": bmi})
```

## SERVER SIDE PROCESSING:

![alt text](<Screenshot 2025-09-26 113604.png>)

## HOMEPAGE:
![alt text](<Screenshot (14).png>)

##OUTPUT:


<img width="1920" height="1080" alt="Screenshot (17)" src="https://github.com/user-attachments/assets/13fa2cde-0535-44e2-ad8f-b93afdaec9ea" />

## RESULT:
The program for performing server side processing is completed successfully.
