# captcha-verifer

Verification your ReCaptcha or HCaptcha is easy

## Installation

```bash
npm i captcha-verifer
```

## Usage

```javascript
Captcha.verifer({
  type: 'hcaptcha', //Required
  secretKey: 'superSecret', //Required
  token: 'TOKEN (Captcha response)', //Required
  ip: '192.109.0.0' //Optional
})
.then(data=>{
  if(!data.success) return; //Captcha not solved

  /* All good. There is your super code! */
})
.catch(e=>console.log(e));
```

Or

```javascript
(async ()=>{
  try{
    const captcha = Captcha.verifer({
      type: 'hcaptcha', //Required
      secretKey: 'superSecret', //Required
      token: 'TOKEN (Captcha response)', //Required
      ip: '192.109.0.0' //Optional
    });

    if(!captcha.success) return; //Captcha not solved
    
    /* Your perfect code here */
  } catch(e){
    console.log(e);
  }
  
})();
```

## Contributing
Any ideas? Contact with me by email iadmaers@icloud.com

## License
[MIT](https://choosealicense.com/licenses/mit/)