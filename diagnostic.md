# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    Router: Create the paths (i.e. 'routes') that will be used to manipulate data throughout the application. These routes are in the form of a URL path.

    Route: Used to direct information throughout the application. Routes primarily consist of directions for the information to flow through.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    'ember generate route campus/boston'
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    {{#link-to 'boston'}} Here's the link to Boston! {{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    1. In the first example, the 'product_id' route is nested under the 'products' route function as opposed to the second example which is not a nested route but has an extended URL path.

    2. The first URL example does not contain the nested path (i.e. the 'products' part) and the second example contains a path that isnt defined as a function and has an unnecissarily long URL (i.e. the 'products' part.)
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    this.route('movie', { path: '/movies/123' })
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    Via the model hook? I'm not exactly understanding the question without an example, I guess?
    ```
