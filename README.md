# IMDb-Movies-TV-Shows-Rating-Finder-Tool
A Node.js and Puppeteer web app that searches IMDb for movies or TV shows and displays their current IMDb rating with a responsive, modern UI.

🎬 IMDb Movies & TV Shows Rating Finder

A simple and modern web application built with Node.js, Express.js, and Puppeteer that searches IMDb for movies and TV shows and displays their IMDb rating.

The application provides a responsive glassmorphism-style interface where users can enter a movie or TV show name, search IMDb, and retrieve the rating automatically.

✨ Features

🔎 Search movies and TV shows by title

🎬 Automatically searches IMDb

⭐ Extracts the IMDb rating

📅 Supports searches containing a year, such as RRR 2022

🤖 Automatically adds movie to simple movie searches for better search accuracy

🌐 Uses Puppeteer for browser automation

📱 Responsive design for desktop and mobile

🎨 Modern glassmorphism UI

⚡ Express.js backend

🛡️ Handles IMDb search failures gracefully

🔄 Displays Working on it when a rating cannot be retrieved

🛠️ Technologies Used

Node.js – JavaScript runtime

Express.js – Web server and routing

Puppeteer – Browser automation and IMDb data extraction

HTML5 – Page structure

CSS3 – Styling and animations

Bootstrap 5 – Responsive styling

Font Awesome – Icons

Google Fonts – Poppins font

📂 Project Structure
imdb-rating-finder/
│
├── server.js
├── package.json
├── package-lock.json
└── README.md


Your JavaScript file can be named server.js or whatever filename you use in your project.

🚀 Getting Started
1. Clone the repository
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git

2. Navigate to the project directory
cd YOUR-REPOSITORY

3. Install dependencies
npm install


The main dependencies are:

npm install express puppeteer

4. Start the server
node server.js


You should see:

✅ Server running at http://localhost:3000

5. Open the application

Open your browser and visit:

http://localhost:3000

🔎 How It Works

The application follows these steps:

The user enters a movie or TV show name.

The Express server receives the search request.

The application checks whether the query contains:

A four-digit year, or

Keywords such as movie, series, or show.

If neither is present, movie is appended to the search query.

Puppeteer opens IMDb's search page.

The application finds the first matching IMDb title.

Puppeteer opens the selected IMDb title page.

The IMDb rating is extracted from the page.

The rating is returned to the web interface.

If the rating cannot be retrieved, the application displays Working on it.

Example

Input:

RRR 2022


IMDb search:

RRR 2022

This can help narrow IMDb search results toward movie titles.

🎨 User Interface

The frontend includes:

Gradient background

Glassmorphism search card

Responsive layout

IMDb-themed styling

Animated buttons

Search icon

Rating display

Mobile-friendly design

⚠️ Important Notes

This project uses Puppeteer to access and extract information from IMDb pages. IMDb's website structure can change over time, which may cause the selectors used by the application to stop working.

For example, the rating selector:

[data-testid="hero-rating-bar__aggregate-rating__score"] span


may need to be updated if IMDb changes its page structure.

The project also includes a fallback that searches the page text for rating patterns such as:

8.3/10

🔐 Puppeteer Configuration

The application launches Puppeteer with several options suitable for running in environments where Chrome sandboxing may cause issues:

args: [
  '--no-sandbox',
  '--disable-setuid-sandbox',
  '--disable-blink-features=AutomationControlled',
  '--disable-dev-shm-usage'
]


Images, fonts, and media requests are also blocked to reduce unnecessary resource loading.

📦 Dependencies
Express

Used to create the HTTP server and handle routes.

Puppeteer

Used to automate a Chromium browser and retrieve information from IMDb.

🔮 Future Improvements

Possible improvements include:

 Display movie title and poster

 Display release year

 Display genre

 Display number of IMDb ratings

 Show multiple search results instead of only the first result

 Add loading animation

 Add error messages for invalid searches

 Add search history

 Add IMDb title links

 Improve IMDb result matching

 Add API-based data retrieval

 Deploy the application online

👨‍💻 Developer

Yashwanth R

Web Development Projects:
https://yashwanthwebproject.netlify.app

📄 License

This project is intended for educational and personal project purposes.

⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub!
