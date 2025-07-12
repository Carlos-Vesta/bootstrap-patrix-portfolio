

#### 1 - INSTALL DEPENDENCIES ####

I - SETTING UP SASS ENVIROMENT
    * Install npm;
    * Install NodeJS;
    * Create a JSON package (to manager all the dependences);
        -> npm init


II - DART-SASS (SASS)
    * Install sass (https://www.npmjs.com/package/dart-sass);
        -> npm install --save-dev sass


III - BOOTSTRAP 5
    * Install bootstrap 5 (https://getbootstrap.com/);
        -> npm install bootstrap@5.3.7 --save


IV - FONTAWESOME
    * Install fonteawesome (https://fontawesome.com/);
     - Start for free
     - NPM

    * Or (https://www.npmjs.com/package/@fortawesome/fontawesome-free);
        -> npm i --save @fortawesome/fontawesome-free

5 - AUTOPREFIXER
    * Install autoprefixer (https://www.npmjs.com/package/autoprefixer);
        -> npm i autoprefixer --save


#### 2 - CREATE NPM SCRIPT TO COMPILE SASS TO CSS ####

    - On the ´package.json´ file, on "scripts": { "test": "echo \"Error: no test specified\" && exit 1" }, remove the script 
    and write your own script;

    - "scripts": {
        "compile:sass": "sass --watch scss:assets/css"
        },
    
    -> npm run compile:sass


#### 3 - CUSTOMIZING BOOTSTRAP ####

    * Create a file "_custom.scss (scss/_custom.scss)" to overrite the default bootstrap styles;
    * Import bootstrap modules to "_custom.scss (@import "../node_modules/bootstrap/scss/bootstrap.scss";)";
    * Import custom sass file "_custom.scss" to the main sass file "style.scss (scss/style.scss)" and use as module (@use 'custom';);
    * Copy the variables to be overrited from "node_modules/bootstrap/scss/_variables.scss" to "scss/_custom.scss";
    * Remove the default flag "!default";
    * Create folders "components" and "sections" inside of scss folder;
    * Create components files inisde components folder:
        - components/_animations.scss
        - components/_buttons.scss
        - components/_mixins.scss
        - components/_typography.scss

    * Create sections files inside sections folder
        - sections/_companies.scss
        - sections/_faq.scss
        - sections/_footer.scss
        - sections/_get-started.scss
        - sections/_intro-section.scss
        - sections/_navbar.scss
        - sections/_portfolio.scss
        - sections/_services.scss
        - sections/_testimonials.scss

    * Import components and sections files to "scss/style.scss"

        // IMPORT THE COMPONENTS
        @use 'components/animations';
        @use 'components/buttons';
        @use 'components/mixins';
        @use 'components/typography';


        // IMPORT THE SECTIONS
        @use 'sections/companies';
        @use 'sections/faq';
        @use 'sections/footer';
        @use 'sections/get-started';
        @use 'sections/intro-section';
        @use 'sections/navbar';
        @use 'sections/portfolio';
        @use 'sections/services';
        @use 'sections/testimonials';



####  PAGES ####

- INTRO PAGE 
    * Downloa Imges with costum colors
        https://www.manypixels.co/gallery

    * Download SVG Waves files
        https://getwaves.io/ 

    * Download Video PopUp
    https://biati-digital.github.io/glightbox/
    https://www.npmjs.com/package/glightbox

        ** How To USe? **
        - Download the file and extract it;
        - Go to dist, copy the css and js folders;
        - Past to your local directory;
        - link the css file (.min) and js file (.min);
        - In the link tag "HTML file" add a class "glightbox";
        - Create a JS script under the script source:
        
            <script src="assets/vendors/glightbox/js/glightbox.min.js"></script>

            <script type="text/javascript">
                const lightbox = GLightbox({

                    'href': 'https://youtu.be/iJKCj8uAHz8?si=_3cVve4LzRSVpKeR',
                    'type': 'video',
                    'source': 'youtube',
                    'width': 900,
                    'autoPlayVideos': 'true',
                });
            </script>  