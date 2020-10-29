# captcha-verifer

Verification your ReCaptcha or HCaptcha is easy

## Advantages

* Without any dependencies
* Less than 5 kb
* ES6
* Verify two types of captcha (ReCaptcha and HCaptcha)
* Ease to use

## Installation

```bash
npm i captcha-verifer
```

## Usage

```javascript
const Captcha = require('captcha-verifer');
```

```javascript
Captcha.verifer({
  type: 'recaptcha', //Required (recaptcha or hcaptcha)
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
    const captcha = await Captcha.verifer({
      type: 'hcaptcha', //Required (recaptcha or hcaptcha)
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

Have a nice day!

## License
[MIT](https://choosealicense.com/licenses/mit/)