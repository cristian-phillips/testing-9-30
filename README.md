# Cloning the branch
git clone git@github.com:PixelatedCodingAdventures/CIS-272.git \
cd to folder and type: \
git checkout develop \
this should bring in all the files.

# Installing
type: npm install \
This should install all the dependencies in package.json

# Environment credentials
credentials for the database are stored in the file ".env" \
Along with ports and DB local ip address.

# db.js
This file is to do with database connection. pulls in info from the .env file.

# app.js
Serves one page or API endpoint (GET /) - (localhost:3000) \
Health check for app + DB (GET /health) - (localhost:3000/health)

# migration.js
Connects to DB + migration \ 
Uploads a basic table from: migrations/001_initial.sql

# tests/app.test.js
Jest tests that: (GET /) and expects: "Equipment Checkout API" \
Jest tests that: (GET /health) and expects: {"app":"up","database":"up"}

# server.js
Launches the webserver

# launch steps
npm run migrate - sends mysql table to DB. \ 
npm test - runs Jest tests. \ 
npm run lint - runs linter (should show nothing if linter passes) \
npm start - starts the webserver