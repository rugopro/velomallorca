# VELOMALLORCA BIKE BUILDER
## _Sitio web de velomallorca donde configurar tu bicicleta por piezas._

## Links

- Desplegar aplicaciones node en vercel
https://dev.to/pabmchn/como-deployar-proyecto-backend-con-nodejs-y-expessjs-en-vercel-3fd0

- Fix: error de base de datos
https://github.com/orgs/vercel/discussions/234

- Subir imágenes a cloudinary con nodejs
https://medium.com/@jatinumamtora/uploading-images-directly-to-cloudinary-from-a-form-in-node-js-6f3a087481b0

## Features 
- MVC
- Postgre SQL database
- JWT security
- Bootstrap and Bootswatch style
- Mustache templating engine

## Dependencies
- [nodejs](https://nodejs.org)
 

## Install
Download repository and install de dependencies
```
git clone git@github.com:RgmDev/velomallorca.git
npm install
```


Rename .env.example to .env and set up the environment
```
NODE_ENV=development
PORT=3000

# ADMIN
ADMIN_MAIL=admin@gmail.com

# DATABASE
#DB_HOST=hostdb
#DB_USER=userdb
#DB_PASS=passdb
#DB_NAME=namedb
DB_POSTGRES_URL="postgresql://user:pass@host.com/dbname"

# JWT
JWT_KEY=secret_key

# MAILER
SMTP_HOST=smtp.gmail.com
SMTP_PORT=465
SMTP_USER=account@gmail.com
SMTP_PASS=password
```

Install seuqelize-cli and migrate database
```
npm install -g sequelize-cli

sequelize db:create
sequelize db:migrate
```

Run de app
```
npm start
```

## Deploy
To deploy in AWS Elastic Beanstalk, create a zip file with the folow items:

```
> app
.sequelizerc
app.js
package.json
```

Then upload the zip file in Elastic Beanstalk and configure de environment vars on AWS.
```
NODE_ENV=production
PORT=8080
DB_POSTGRES_URL=postgreurl
JWT_KEY=jwtkey
```