
---
layout: article
title: "Email BackEnd with SMTP Gmail"
date: 2018-01-13 19:45:00+0200
coverPhoto: https://github.com/boubli/Youssef-Boubli/blob/gh-pages/contents/images/2019/01/Opencv-python.png?raw=true
---

Add this configurations in your `settings.py`

This configurations is if you work with `smtp.gmail.com`, other smtp is similiar with configurations.

* Unlock Captha: [https://accounts.google.com/DisplayUnlockCaptcha](https://accounts.google.com/DisplayUnlockCaptcha)
* Change to active: [https://www.google.com/settings/security/lesssecureapps](https://www.google.com/settings/security/lesssecureapps)

```
EMAIL_HOST          = 'smtp.gmail.com'
EMAIL_PORT          = 587
EMAIL_HOST_USER     = 'your_gmail@gmail.com'
EMAIL_HOST_PASSWORD = 'your_password'
EMAIL_USE_TLS       = True
DEFAULT_FROM_EMAIL  = EMAIL_HOST_USER
EMAIL_BACKEND       = 'django.core.mail.backends.smtp.EmailBackend'
```