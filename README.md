# Web App with Postgres Database using Flask + React.
In this example, we will create a web app which displays two images side by side and the user is asked to select one, updating a database.
For more detail: https://medium.com/@emilymuller1991/developing-a-web-app-with-postgres-database-using-flask-react-9c297606aed9.

## Summary 
1. Postgres Database
2. Flask API for back-end
3. React for front-end
4. Google Street View API key

## Requirements
* postgres
* flask, psycopg2, flask-cors
* node.js, react-youtube, react-bootstrap
 
### Postgres DB
Install postgres: https://www.postgresql.org/download/.

Create DB 'example' as user postgres.

Dump example data:
```
web-app/sql$ psql -U postgres example < ratings
web-app/sql$ psql -U postgres example < images
```

### Flask Back-end
``` pip install requirements.txt ```

Set environmental variables:
```
export app_host='localhost'
export db='example'
export db_user='postgres'
export db_host='localhost'
export db_port=5432
```
run: 
```web-app/back_end$ python app.py```

### React Front-end
Install node.js: https://docs.npmjs.com/downloading-and-installing-node-js-and-npm.

Set environmental variables in new file web-app/front_end/.env:
```
REACT_APP_BACK_END_HOST ='localhost'
REACT_APP_BACK_END_PORT = '5000'
REACT_APP_API_KEY = 'API_KEY_from_GOOGLE_STREET_VIEW_API'
```
Get api key from Google Console: https://console.cloud.google.com.

run: 
```web-app/front_end$ npm install```

run: 
```web-app/front_end$ npm start```



