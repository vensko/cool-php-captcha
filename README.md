# cool-php-captcha
This is the official GitHub project from code.google.com/p/cool-php-captcha



This project generates friendly captcha images. This project provides the SimpleCaptcha class.
Some fetures are: Background and foreground colors, dictionary words, non-dictionary random words, blur, shadows, JPEG and PNG support.


Basic example:
--------------


```
session_start();
$captcha = new SimpleCaptcha();
// Change configuration...
//$captcha->wordsFile = null;           // Disable dictionary words and use random letters instead
//$captcha->wordsFile = 'words/es.txt'; // Enable spanish words dictionary
//$captcha->session_var = 'secretword'; // Changes the session variable from 'captcha' to 'secretword'
$captcha->CreateImage();
```

... will output an image.



You can validate the php captcha with: (case-insensitive version)

```
if (empty($_SESSION['captcha']) || strtolower(trim($_REQUEST['captcha'])) != $_SESSION['captcha']) {
    return "Invalid captcha";
}
```

You can see a live example here: http://joserodriguez.cl/cool-php-captcha





