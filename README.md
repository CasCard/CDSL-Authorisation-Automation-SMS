# CDSL-Authorisation-Automation-SMS

This is an updated version of CDSL OTP Verification that directly fetches OTP from SMS using [https://messages.google.com/](https://messages.google.com/) which is a service by Google which enables you to view SMS in your mobile directly in a web-browser.

## Setup

### 1. Installing ```Messages``` App from Play Store

![Screenshot_2021-06-13-23-40-59-34](https://user-images.githubusercontent.com/13176032/121817774-0627ba80-cca1-11eb-876e-d5bbfd643c38.jpg)

Once install you need to make it as your default messaging app.

### 2. Pairing with browser

Navigate to [https://messages.google.com/web/authentication](https://messages.google.com/web/authentication) .

Enable ```Remember this computer``` and you can scan the QR code using the Messages app

![Screenshot 2021-06-13 234433](https://user-images.githubusercontent.com/13176032/121817825-5737ae80-cca1-11eb-98b1-9eee1f97446b.png)

Now you will be able see the messages in your smartphone within [https://messages.google.com](https://messages.google.com)

You can close the window and again navigate to [https://messages.google.com](https://messages.google.com) ,to ensure that the PC is remembered.

### 3. Download Chrome Web Driver

Find the version of the chrome that you are using by navigating to ```chrome://settings/help``` or
```Setting > About Chrome```

Download [Chrome Webdriver](https://chromedriver.chromium.org/) corresponding to your version.
Currently it is ```90.0.4430```.

### 4. Download Python

If you haven't installed python earlier you can download setup from [here](https://www.python.org/downloads/)

### 5. Install Necessary Packages

Download all the files present in this repository and place them is a separate folder, Chrome Driver ```exe``` file should also be present in the same folder.

Open a new terminal in the same directory and install necessary packages with the following command

``` pip install -r requirements.txt```

### 4. Configuring Chrome Profile and CDSL Pin

This script's allowes Selenium to use the Chrome's Default profile.This helps in not re-entering Kite Username and Password as they will be automatically populated in the requred fields by Chrome's autofill feature. 

To ensure that ,when you open [https://kite.zerodha.com/](https://kite.zerodha.com/) you will be able to see your default user and there will be only option to enter password and obvisouly it will be filled by Chrome Auto Fill.

You can save your ```Kite``` password in Google Chrome's save password feature so it would automatically populates the ```Kite``` login screen with password.


Open ```config.py``` in a text/code editor.

Enter your ```CDSL``` PIN.

If Kite is configured for 2FA with Google Authenticator the process will be unsuccessful.

### 5. Usage

Once you have completed the setup opens a new terminal in the same directory containing the required files and type:

```python authorisation.py```

you only needed to type this command whenever authorisation is necessary

## Issues
Feel free to create a new issue in cause of any trouble will be happy to resolve.

## Contributing
Pull requests are welcome.
## License
[MIT](https://choosealicense.com/licenses/mit/)
