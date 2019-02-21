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

