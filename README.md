This is the source code for Prof. Jakob Eriksson's personal webpage, viewable at http://www.cs.uic.edu/~jakob. 
Feel free to fork this repo to make your own UIC-themed webpage. 

To use it, first install node. On a mac, that would be 
`brew install node`. On linux, `apt-get install nodejs npm`. 

Then install the static site generator 11ty and the CSS framework tailwind. 
`npm install -D @11ty/eleventy tailwindcss@latest`

To use this as a template, start by updatin the settings in `_data/defaults.json' to reflect your name, title and a suitable portrait. Delete the contents of 'photos/' and add some of your own. Use landscape oriented photos of high resolution, and with your face fairly prominent and centered. Then, simply edit `home.md`, `projects.md` and `news.md` with your own content, and you're good to go.

To try it out, run `npm start` in the main folder, and open your website in a browser using the URL `localhost:8080`.