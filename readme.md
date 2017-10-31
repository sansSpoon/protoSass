## protoSass Setup
This is a no-brainer sass-testing setup. I created it so I can pull down a basic template to run Sass ideas from. There are minimal dependancies for npm, no taskrunners, and nothing to get in the way.

Super simple usage:

`npm start`


### The template was created with
-	create a base directory `mkdir protoSass`
-	`cd protoSass`
-	create this file as `touch readme.md`
-	create the sass file `mkdir _sass && touch _sass/main.scss`
-	create the css file `mkdir -p public/css && touch public/css/main.css`
-	create the html file  `touch public/index.html`
	-	Use the simplified html boilerplate in my snippets library
	-	`cat _snippets/html/_html5.html > index.html`
	-	link the generated css file
-	setup the package `npm init`
	-	removed the *main* node as it is not needed here
	-	specify GitHub repo `https://github.com/sansSpoon/protoSass.git`
	-	default everything else
	-	added the script entry
		-	`sass --watch _sass/:public/css/`
-	created the git repo with `git init`
	-	`git config user.name "sansSpoon"`
	-	`git config user.email "sans.spoon@gmail.com"`
	-	`printf ".DS_Store\n.sass-cache\n" > .gitignore`
	-	`touch public/css/.gitkeep`
	-	`git add .`
	-	`git commit -m "Initial Commit"`
	-	`git remote add 'github' https://github.com/sansSpoon/protoSass.git`
	-	`git push -u github master`

## Version Info
-	1.0.0.
	-	Initial Build
	-	basic npm wrapper for Sass
	
-	1.1.0.
	-	adds Autoprexifer using postcss-cli
	-	start command runs scripts in parallel