# [UBGI]()

## A Tool for Incorporating Eye Tracking Data in RPA: Enhancing User Behavior Logs

Manuel García-Romero (orcid=0000-0003-2113-3497) (mgarcia44@us.es)
Antonio Martínez-Rojas (orcid=0000-0002-2782-9893) (amrojas@us.es)
A. Jiménez-Ramírez (orcid=0000-0001-8657-992X) (ajramirez@us.es)
J. G. Enríquez (orcid=0000-0002-2631-5890) (jgenriquez@us.es)

University of Seville. Computer Languages and Systems Department. E.T.S. Ingeniería Informática. Avenida Reina Mercedes, s/n, 41012, Seville, Spain}

Proceedings of the Demonstration \& Resources Track, Best BPM Dissertation Award, and Doctoral Consortium at BPM 2024 colocated with the 22th International Conference on Business Process Management, BPM 2024, Krakow, Poland, September 1-6, 2024

<br />

## Demo

> Create a new user on the **registration page** or executing in the terminal "python manage.py createsuperuser".

> Recommendation -> User:demo;Password:demoBPM2024

> The demo video is at 


<br />

## Quick start

```bash
$ # Get the code
$ git clone https://github.com/RPA-US/ubgi.git
$ cd ubgi
```

> After getting the code, open a terminal and navigate to the working directory, with product source code.
> The following software is needed to run this platform if you want to install via local:
- Python 3.10 or newer
- Install PostgreSQL
- C++ Dev Tools from Visual Studio: ![visual_studio_c++_features](apps\static\assets\img\image.png) 

> You can install ugbi via docker if you do not want to install ugbi,python and PostgreSQL locally. 
``` bash
$ docker-compose -f docker-compose-dev.yml up
```
Remember to attach the container in VS code and install python for that container instance.


```bash
$ # Virtualenv modules installation (Unix based systems)
$ virtualenv env
$ source env/Scripts/activate
$
$ # Virtualenv modules installation (Windows based systems)
$ # virtualenv env
$ # .\env\Scripts\activate
$
$ # Install modules - SQLite Storage
$ pip install -r requirements.txt
$
$ 
```

> Copy the content from ".env.sample" and paste it in a new ".env" . This ".env" must be placed in ubgi/core. Change the values if you need it

```bash

$ python manage.py makemigrations apps_analyzer apps_behaviourmonitoring apps_featureextraction apps_notification
$ python manage.py migrate
$
$ 
$ python manage.py createsuperuser 
$
$ # Start the application (development mode)
$ python manage.py runserver # default port 8000
$
$ # Start the app - custom port
$ # python manage.py runserver 0.0.0.0:<your_port>
$
$ # Access the web app in browser: http://127.0.0.1:8000/
```

> Note: To use the app, please access the registration page and create a new user. After authentication, the app will unlock the private pages.

## Eye Tracking Use and Support

To record a gaze log with the eye tracking software integrated into ScreenRPA (WebGazer.js <https://github.com/brownhci/WebGazer>), follow these steps:

1. **Start the UGBI Web Application**
   - Launch the UGBI web application.

2. **Access WebGazer**
   - Click on "Access to WebGazer" to open the WebGazer.js suite.

3. **Prepare Your Case Study Scenario**
   - Arrange all the applications you will interact with in windowed mode.
   - Ensure the UGBI tab in your browser is open and in the background.

4. **Start Recording**
   - Begin recording the UI Log usingStepRecorders.
   - Then, click on "Start" in the WebGazer suite to record the Gaze Log.

5. **Perform Your Activity**
   - Stay calm and perform your activity naturally. UGBI will handle the rest, recording both your UI log and Gaze Log!

By following these steps, you will effectively utilize the eye tracking capabilities of UGBI to capture comprehensive logs of your interactions.


