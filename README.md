# M4-D6

Netflix, React Edition + React Strivebooks Library
In this exercise you'll apply your new knowledge about component lifecycle to improve Strivebook App & Netflix App.


StriveBooks App
Make sure to refactor the grid of the books list to have the list on the left and the CommentsArea always visible on the right.
Create the initial state for the CommentsArea for when there's no data to be displayed.
The CommentsArea behaviour: every time the user clicks on a card a fetch should be perfomed and comments should update. Pass the single ID property and let the Component handle the fetch by using the componentDidUpdate method.



Netflix App
Implement loading states (placeholders) for movie cards while fetch is awaiting response. TIP: use the network tab to simulate a slow internet connection. Visit: https://developers.google.com/web/tools/chrome-devtools/network#throttle
Change the SearchBar behaviour. Now the fetching of the information shall be responsability of the MovieList component. Pass the "search query" property and let the Component handle the fetch by using componentDidUpdate method.
Add CommentsList for each movie if you didn't already. This comment list should be a section always visible in the page. The fetching of the information shall be responsability of this CommentsList component. Pass the single ID property and let the Component handle the fetch by using componentDidUpdate method. N.B. If instead you've already created modals for that, work on those to have them use the componentDidUpdate method.
EXTRA
Work on Loaders, error messages, empty states
Improve the style of your App
      
        NETFLIX API INFO:

        Register to http://www.omdbapi.com/

        Once registered, you'll receive via email an api key.
        The API has a search method:

        http://www.omdbapi.com/?apikey=[YOUR API KEY HERE]&s=harry%20potter

        This search returns an object like this:

        {
        "Search": [
            {
                "Title": "Harry Potter and the Deathly Hallows: Part 2",
                "Year": "2011",
                "imdbID": "tt1201607",
                "Type": "movie",
                "Poster": "https://m.media-amazon.com/images/M/MV5BMjIyZGU4YzUtNDkzYi00ZDRhLTljYzctYTMxMDQ4M2E0Y2YxXkEyXkFqcGdeQXVyNTIzOTk5ODM@._V1_SX300.jpg"
            },
            {
                "Title": "Harry Potter and the Sorcerer's Stone",
                "Year": "2001",
                "imdbID": "tt0241527",
                "Type": "movie",
                "Poster": "https://m.media-amazon.com/images/M/MV5BNjQ3NWNlNmQtMTE5ZS00MDdmLTlkZjUtZTBlM2UxMGFiMTU3XkEyXkFqcGdeQXVyNjUwNzk3NDc@._V1_SX300.jpg"
            },
            {
                "Title": "Harry Potter and the Chamber of Secrets",
                "Year": "2002",
                "imdbID": "tt0295297",
                "Type": "movie",
                "Poster": "https://m.media-amazon.com/images/M/MV5BMTcxODgwMDkxNV5BMl5BanBnXkFtZTYwMDk2MDg3._V1_SX300.jpg"
            },
            {
                "Title": "Harry Potter and the Prisoner of Azkaban",
                "Year": "2004",
                "imdbID": "tt0304141",
                "Type": "movie",
                "Poster": "https://m.media-amazon.com/images/M/MV5BMTY4NTIwODg0N15BMl5BanBnXkFtZTcwOTc0MjEzMw@@._V1_SX300.jpg"
            },
            {
                "Title": "Harry Potter and the Goblet of Fire",
                "Year": "2005",
                "imdbID": "tt0330373",
                "Type": "movie",
                "Poster": "https://m.media-amazon.com/images/M/MV5BMTI1NDMyMjExOF5BMl5BanBnXkFtZTcwOTc4MjQzMQ@@._V1_SX300.jpg"
            },
            {
                "Title": "Harry Potter and the Order of the Phoenix",
                "Year": "2007",
                "imdbID": "tt0373889",
                "Type": "movie",
                "Poster": "https://m.media-amazon.com/images/M/MV5BMTM0NTczMTUzOV5BMl5BanBnXkFtZTYwMzIxNTg3._V1_SX300.jpg"
            },
            {
                "Title": "Harry Potter and the Deathly Hallows: Part 1",
                "Year": "2010",
                "imdbID": "tt0926084",
                "Type": "movie",
                "Poster": "https://m.media-amazon.com/images/M/MV5BMTQ2OTE1Mjk0N15BMl5BanBnXkFtZTcwODE3MDAwNA@@._V1_SX300.jpg"
            },
            {
                "Title": "Harry Potter and the Half-Blood Prince",
                "Year": "2009",
                "imdbID": "tt0417741",
                "Type": "movie",
                "Poster": "https://m.media-amazon.com/images/M/MV5BNzU3NDg4NTAyNV5BMl5BanBnXkFtZTcwOTg2ODg1Mg@@._V1_SX300.jpg"
            },
            {
                "Title": "Harry Potter and the Chamber of Secrets",
                "Year": "2002",
                "imdbID": "tt0304140",
                "Type": "game",
                "Poster": "https://m.media-amazon.com/images/M/MV5BNTM4NzQ2NjA4NV5BMl5BanBnXkFtZTgwODAwMjE4MDE@._V1_SX300.jpg"
            },
            {
                "Title": "Harry Potter and the Forbidden Journey",
                "Year": "2010",
                "imdbID": "tt1756545",
                "Type": "movie",
                "Poster": "https://m.media-amazon.com/images/M/MV5BNDM0YzMyNGUtMTU1Yy00OTE2LWE5NzYtZDZhMTBmN2RkNjg3XkEyXkFqcGdeQXVyMzU5NjU1MDA@._V1_SX300.jpg"
            }
        ],
        "totalResults": "80",
        "Response": "True"
      }

    

    
        STRIVEBOOKS COMMENTS API INFO:

        You have a CRUD endpoint for comments on:

        https://striveschool-api.herokuapp.com/api/comments/

        This means you can GET, DELETE, POST, PUT data from there.

        The Comment structure is this:

        {
          "comment": "A good movie but definitely I don't like many parts of the plot",
          "rate": 3,
          "elementId": "tt1756545"
        }

        Where:
        - comment is the comment inserted by the user
        - rate is a value between 1 and 5
        - elementId is the imdbID of the movie / serie

      
    
