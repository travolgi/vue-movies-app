# Vue Movies app

Search Movies and Series

## Table of contents

- [Overview](#overview)
- [Process](#my-process)
  - [Built with](#built-with)
  - [Structure of the project](#structure-of-the-project)
  - [Useful resources](#useful-resources)
- [License](#license)

## Overview

Created entirely from scratch

- Search for movies and TV series to watch
- Sort by different criteria
- Save the best in localStorage
- See details of movies saved
- Dark / light mode
- API data

![Vue Movies app]()

## Process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- Vanilla Javascript ES6
- [Vue](https://vuejs.org/) - JS library
- Fetch API
- [RapidAPI](https://rapidapi.com/apidojo/api/imdb8/) - API data
- localStorage

### Structure of the project

Responsive design is handled with **Vanilla javascript**:
- below `800px` the sidebar is moved inside the navbar button
- when you go down `100px` in the film container, the scrool to Top button appears

**Vue** manages:
- dark-light mode change
- data recovery via `fetch`
- sorting of data according to different criteria
- the opening of the `modal` of the details of the film
- saving or removing saved movies
- various other helper methods

If `fetch` returns error **429**, fake test data will be shown, otherwise it will show the data of the call made, sorted by default in chronological order. The 50 most popular films of the moment are initially recovered.

The saving takes place on `localStorage` and through the page of the saved movies you can see the details of each movie by opening a modal and an `API` call made through the movie `id`.

I used the `callAPI` method for calling any **endpoint** and then handling the various cases via `switch`. The idea was to create a single helper with input parameters without repeating code for the different calls. 

Source data from `API` of [imdb8](https://rapidapi.com/apidojo/api/imdb8/) - RapidAPI. 

### Useful resources

- [RapidAPI](https://rapidapi.com/apidojo/api/imdb8/) - Source data movies

## License 
Vue is [MIT license](https://github.com/vuejs/vue/blob/dev/LICENSE)  
RapidAPI has different [pricing plans](https://rapidapi.com/apidojo/api/imdb8/pricing)