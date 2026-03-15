Project structure: the webapp follows a MVC architecture using Node.js, Express, and MySQL.

The submission files include:
app.js: initializes the Express server, configures session management, and sets up the middleware.
db.js: handles the database connection pool.
.env: contains environment variables and database credentials.
routes/: contains the backend logic and API endpoints, such as routes/auth.js handles login/logout logic, while routes/rides.js manages ride operations.
views/: contains the frontend templates rendered by EJS.
middleware/: contains custom middleware functions to enforce role based access control.
public/: stores images for the front page.
submission_dump.sql: complete SQL export of the database. Includes the schema, stored procedures, triggers, and populated sample data.
ca.pem: contains certificate for connecting to the database.

To install the project:

1. Connect to database:
	- Open MySQL Workbench and create a new connection.
	- Enter the Connection Details: 
		Hostname: 	mysql-254204d6-curaturae-12be.f.aivencloud.com
		Port: 		22523	
		Username: 	avnadmin
		Password: 	AVNS_G8_3Eyw9XAf1ZYbd8BQ
	- Go to SSL tab.
	- On the "SSL CA File" field, browse and select "ca.pem" file.
	- Click "OK".
	- Import data using "submission_dump.sql"
	- On success, changes to the frontend can be verified here.

2. Run the web app:
	A. Use the hosted link, no setup required: https://theme-park-app.onrender.com/
		- Data changes on the frontend can be verified in the database if connected in step 1.

	B. Setup the webapp locally:
		1. Unzip the code base if not already done so.
		2. Open terminal in the root directory.
			- Install dependencies: "npm install"
			- Start the server: "node app.js"
		3. Open the browser to http://localhost:3000
			- .env is already configured to connect with the database.

Logins:
- Default password for all accounts below: "Clubhouse123"

- Username for roles:
	Admin: 							walt@park.com
	Park manager: 					minnie@park.com

	Location manager (main entrance):	mickey@park.com
	Staff (main entrance): 				daisy@park.com

 	Maintenance 1:					goofy@park.com
 	Maintenance 2:					bob@park.com 	
 	Maintenance 3:					felix@park.com
 	Maintenance 4:					manny@park.com
 	Maintenance 5:					doc@park.com

- Can also log in as any other employee found in the "Park Employees" list using their email and the default password "Clubhouse123".