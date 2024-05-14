# Restaurant_Web

## Description:

Our website offers a guide to restaurant reviews, covering a vast range of international cuisines, food types, and price points. From affordable eats to luxury dining, users can discover new restaurants through detailed reviews and ratings. Whether you're in the mood for comforting Italian pasta, fiery Thai curry, or a classic American burger, our platform makes it easy to find the perfect dining spot.





## How to use the webpage:

The webpage has a pretty straightforward interface and functionality. If there is any questions, an easy solve is to use the AI chatbox for how the filter and backend work. 





## Here is a breakdown in words as well:

Choose Cuisine Types: Start by selecting food categories, like Italian or American. You can select multiple to broaden your search.
Specify Your Budget: Filter restaurants by price range using the options: $ (inexpensive), $$ (moderate), $$$ (pricey), or $$$$ (high-end). Combine this with cuisine types to match both your taste and budget.
Refine Your Search: For targeted results, combine food categories with specific features. Selecting "American" and "Burgers," for instance, filters for American burger joints.
Sort Results: Organize your findings with the "Sort By" function. Choose to view recommendations based on a mix of ratings and reviews or opt for the highest-rated restaurants.
Use the Chat Feature: Click the chat box for immediate assistance. For example, you can ask on the chat box about “tell me more about the webpage”.
See Reviews: Access detailed reviews and ratings for each restaurant. You can see what others have to say about their dining experiences, including the number of reviews.





## Frontend/backend interaction:

The front end page is three components, the chatbox with an ai explainer, the filters, the corresponding restaurants.
Through a variaty of javascript functions, the filters that are ticked by a user are sent to the backend file routes.py to retrive information from the data base. 
The most important frontend and backend interaction is how selected filters retrive information through the database operations in the backend. 
Here is how it's done:
1. The event listeners (each event listener should be commented well in the home.html file) will updata the active filter dictionary and call the js function updateFiltersAndFetchData()
2. When the funtion updateFiltersAndFetchData() is called, the updated active filter will be posted to the "/filter" route where the filter() function will call the database operation function fetch_restaurants_with_reviews() to retrieve data. 
3. The function construct and execute sql queries based on the filter information that is passed in. Then, the retrived data are converted in Json format for the defined routes in route.py to return to the front end. 
4. To return the filter restaurants to the frontend, in the same updateFiltersAndFetchData() function after "/filter" returns the data, updatePageContent(data); updateRestaurantDescriptions(); updateRatings() (three other js functions) are called which will update the page. 
These steps construct the main function of our page. 

Some auxiliary functions are dynamically displaying starts and half start, collapsing the description of a restaurant and filter buttons, and the openai chatbox that explain the webpage. These functions are pretty straightforward and commented well to denote their function. 
