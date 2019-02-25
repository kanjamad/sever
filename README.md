## Make a server 
I need a server something that the front-end can communicate with so that this app can live on more than just my laptop

## start with the basic
                npm init -y

Yay!! I have my package.json 

                npm install --save-dev nodemon
                npm install express
                npm install body-parser

I install 
	Express framework - so that I can build a server really nice.
	Nodemon - so I can run Nodemon in my scripts and make sure my server is running.
	body-parser - which I use to parse and have access to the [req.body] to read JSON and form data.

## package.json
                "start": "nodemon server.js"
And now every time 'nmp start' my server will run

## Planning 

I do before start coding and I want to make sure that I have an idea of what my API design will look like, what I want to create.

                            --> res = this is working
                            signin --> POST = success/fail
                            register --> POST = user
                            profile/:userId --> GET = user
                            image --> PUT --> user

## Express 
come with a built in JSON method on response that I can use 

## Storing User Passwords
Security is a very important thing on the web.
Here I wanted to show the recommendations for storing user passwords and improving security Learn more  [Andrei Neagoie](https://www.udemy.com/share/100HQLBEYdcF5URX4=/)
Step 1:
It all begins when you ask your user to create an account by setting a username and password. This is where user experience will need to play nicely with proper security measures. United States National Institute for Standards and Technology (NIST) is currently finalizing their recommendations for password management. Some of these include:

1. Your minimum password length should be at least 8 characters, and the maximum as large are 64 characters for the user. The longer the password that the user sets, the better. This will also play nicely if said user is using password managers like 1Passwordsince their generated password will be long and fit this criteria. There is nothing worse than the password limit being too small for a password generated by 1Password.

2. Do accept both ASCII and UNICODE characters and don't set rules about which characters should and shouldn’t be included (P@ssword1 is NOT a good password). Instead, encourage people to set long passwords with high entropy (upper case letters, lower case letters, digits, special characters).

3. Don’t allow password hints.

4. Avoid security questions. Although this is good for an extra layer of security, the information can be easily discovered by an attacker in this day and age. It’s just an extra implementation step; a step that a user has to take while offering very little added security. Yahoo had this information stolen-- which was saved in plain text, allowing the attacker to easily see this information about each user.

5. Use 2FA (2 factor authentication) if you want an extra layer of security in your application, but avoid using SMS as this can be easily hacked to have the attackers phone receive the confirmation code.
