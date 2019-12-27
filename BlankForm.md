# Applicant Name
Key:
:black_square_button: -> unasked question
:white_check_mark: -> Correct Answer
:ballot_box_with_check: -> Partially Correct Answer
:x: -> Incorrect Answer
---

## PHP Questions:

### :black_square_button: Explain the difference between $_GET and $_POST
> $_GET contains "http GET" request data, for instance the key/value pairs in the querystring. $_POST contains the data from an "http POST" request. 

### :black_square_button: What is the difference between a while loop and a do-while loop?
> A while loop will run as long as the condition is true, a do-while loop will always run at least once and then run while the condition is true.

### :black_square_button: When working with a database, either with PDO or MySQLi, what do prepared statements help with?
> They prevent SQL Injection by limiting the query to the type intended and binding user inputted data to the correct positions.

### :black_square_button: Can you give an example of cross site scripting?
> If user inputted data is being stored in a database and isn't being sanitized before being displayed on a page, a user can inject HTML or Javascript into the database that then gets loaded onto your site. This could potentially be a form that collects credit card info under the guise of a subscription renewal form and posts it off to an external site, thus allowing them to steal credit card info.

### :black_square_button: What is tyhe difference between a trait and an interface?
> An interface is like a contract or "promise" to implement certain methods in a class where a trait contains the actual implementation in it already.

### :black_square_button: What is the difference between include and require?
> Include will emit a warning on a missing file, require will emit a fatal error on a missing file.
#### :black_square_button: Follow-up: What is the difference between require and require_once?
> Require Once will check to see if the file has already been included, and if it has, not include it again.

### :black_square_button: What is a recursive method?
> Any method that calls itself from within the body of the method. i.e.

    public function add($n) {
        return $n + add($n); //infinitely recursive.
    }

---

## Laravel Questions:

### :black_square_button: How would you make a model in Laravel?
> php artisan make:model [options] ModelName

### :black_square_button: What is the purpose of the .env file?
> Stores environment variables
- Elaborate?
> Stores environment variables specific to a development/production environment, for instance a local DB host at 127.0.0.1 for dev or a production DB etc.

### :black_square_button: How would you express (in a method) that a model is the child in a one-to-many relationship with another model?
> it will have a method returning $this->belongsToMany() ...

### :black_square_button: Can you give me an example of a polymorphic relationship in laravel?
> Address model that can be owned by multiple types of models in the system like users, orders, companies, etc.

### :black_square_button: If you have a bunch of search results but you only want to display 25 per page, how would you handle that?
> Fetch the data with paginate method instead of get(). $results->paginate(25)

### :black_square_button: What does the @can blade directive do?
> Checks with a model policy to see if a model can perform the specified action before rendering the given html.

### :black_square_button: What blade directive will let you iterate over a collection of data in the template file?
> @foreach or @forelse, maybe @for if explained properly.

---

## Basic Database Questions:

### :black_square_button: What is a basic query to pull all rows from the table "A" that has the value 123 in column "C"
> SELECT * FROM A WHERE C=123;

### :black_square_button: What does a left join do?
> Selects all data from the "left" table and all matching data from the right table.

### :black_square_button: What type of query would you use to add data to the database?
> INSERT