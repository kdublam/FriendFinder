![hw-13-logo](http://vivalifestyleandtravel.com/cached/download/v1517600397/vivafront/j5onyvky961zpnkkj3sj.jpg)

Welcome to Central Perk Cafe. Have you ever wonder if those 6 kids that are always hanging out on the couch might be your best friend or better yet, your lover? Well now you can find out for yourself! Take our survey and our algoritm will find your perfect match.

## Live Link
 - https://central-perk-matchmaker.herokuapp.com/

## Usage

To find your match, simply navigate to the survey page using the link above. Take the survey (make sure all questions are answered) and you will be matched with a new friend! 

## Requirements
- Modularity in the form of separate files for server logic, storing of friends, views, and routing
- 10-question survey to assess uniqueness of users
- Use `express`, `body-parser`, and `path` npm packages in the `server.js` file
- Separate JavaScript files for routing (`htmlRoutes.js` and `apiRoutes.js`)
- Appropriate GET and POST routes for serving HTML pages and API calls
- Separate file for storing friends PUN INTENDED (`friends.js`)
- Calculate best match for user once survey is completed and return that match to the user

## Technologies Used

- JavaScript
- jQuery
- Node.js
- Express.js
- HTML
- Bootstrap

## Code Explanation
- Our `server.js` file sets up the Express server, specifying our port number, the npm packages that need to be loaded, and also the routes, which we have externalized
- There are 2 separate HTML files (`home.html` and `survey.html`) that serve as the front-end portion of our code; they determine what the user sees (the homepage and the survey, which will also show the resulting best match)
- Our 2 routing files (`htmlRoutes.js` and `apiRoutes.js`) determine the back-end logic (based on the request being made, the response that gets sent to the browser); the HTML routes display the survey and the homepage based on the URL that is accessed, and the API routes send back existing content in our server-side data or add new friends
- Best match is calculated by finding the friend with the minimal difference in scores and then sending that friend to the browser as a JSON object
- A modal is then toggled, displaying the the best match to the person who just took the survey
- In essense, this will also be a form of notes that you may later reference weeks later
- Friends are stored as such:

```js
{
	name: "Joey",
		photo: "https://upload.wikimedia.org/wikipedia/en/d/da/Matt_LeBlanc_as_Joey_Tribbiani.jpg",
		scores: [5, 1, 2, 3, 1, 2, 5, 1, 1, 1]
}
```