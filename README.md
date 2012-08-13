## Header 2 ##

* Bullet
* Bullet

1. Number
2. Number

### Create ###

    openssl req -new -x509 -key privkey.pem -out cacert.pem -days 1095
    openssl req -new -x509 -key privkey.pem -out cacert.pem -days 1095  
    
## Deployment

### Heroku
Environment specific settings will have to be set as [Config Vars](https://devcenter.heroku.com/articles/config-vars).
Set each environment variable required (see [Required Environment Variables](#required-environment-variables)).
Special note about google private keys: since storing files is not allowed on Heroku, you will have to set
your private key as an encoded PEM string. To set a multi-line
envirnoment variable on heroku, use the following command: 
    heroku config:add GOOGLE_CLIENT_KEY="-----BEGIN RSA PRIVATE KEY-----
    ...
    -----END RSA PRIVATE KEY----- 
    " --app $app_name