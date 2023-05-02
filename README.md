# Tinder Of Food
This project is a Flask interactive web application that displays a map of New York City and allows users to query it, along with a recommendation algorithm that matches suppliers to restuarants. The application uses a combination of Python, html, css, and Javascript. The data is stored using Apache Spark and MongoDB.

The website includes three route functions - /, /map, and /match (with GET and POST methods). 
The first route function, index(), renders a map template file and displays a map of New York City with some markers. It returns the index.html template with the map embedded. The map retrieves data from Apache Spark, which stores business data such as name, rating, price range, hours of operation. Then, for every restuarant the highlighted reviews are retrieved from the MongoDB database.

The map() function also renders a map template file with the same functionality as the index() function.
The post_map() function takes user input from the map form and queries a database to return the matching results. It then renders a new map with the matching markers.
The function uses the requests module to retrieve data from the database and create markers and popups on the map. 

The application also uses recommendation algorithms to match suppliers with restaurants using the post_match() function. Here, I created a recommendation algorithm that queries the Spark dabase based on the supplier profile information.
