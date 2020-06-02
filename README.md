1)Module requirements:

  "dependencies": {
    "bcryptjs": "^2.4.3",
    
    "cookie-session": "^1.4.0",
    
    "express": "^4.17.1",
    
    "jsonwebtoken": "^8.5.1",
    
    "mongodb": "^3.5.7",
    
    "mongoose": "^5.9.14",
    
    "multer": "^1.4.2",
    
    "passport": "^0.4.1",
    
    "passport-google-oauth2": "^0.2.0",
    
    "sharp": "^0.25.2",
    
    "validator": "^13.0.0"
  },
  
  "devDependencies": {
    "env-cmd": "^10.1.0",
    
    "jest": "^26.0.1",
    
    "nodemon": "^2.0.4",
    
    "supertest": "^4.0.2"
  }
  
 2) Run POC :
=>npm init (Create npm modules) and install required modules 

=>type "npm run dev" in terminal to intiate nodemon where index.js intialize the project and than
	server will set on given PORT number in dev.env file

=>Visit this URL to login in google account :   localhost:3000/auth/google  

=>Now,You have to login first by gmail account .Once you sign in ,session begin on given cookie in keys.js file in config

=>You have to use POSTMAN for rest of endpoints except "logout".

=>set request headers in POSTMAN "Authentication=generated token of user at the time of login"
(You can find token in user's profile once it is login in database)

=>You have to logout the session from browser using given URL :   localhost:3000/api/user/logoutUser/

Note: POSTMAN can run "localhost:3000/api/user/logoutUser/"  but  "req.logout()" not working in controller of "/logoutUser" 
when we run in POSTMAN. Here,we have to use browser to logout the session.  
	
3)TEST the endpoints:
=> type "npm test" to run the test cases	
