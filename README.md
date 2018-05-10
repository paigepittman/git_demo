
## Giphy Filter - React review

run create-react-app [name of app]

cd into the src folder and create a directory called children. Inside children create two new components: Search and Results

In public > index.html add the bootstrap CDN:
  <!-- <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0-beta.3/css/bootstrap.min.css" integrity="sha384-Zug+QiDoJOrZ5t4lssLdxGhVrurbmBWopoEl+M6BdEfwnCJZtKxi1KgxUyJq13dy" crossorigin="anonymous"> -->

In App.js add some bootstrap:
<div className="jumbotron"><h2>Giphy Filter</h2>
  </div>
<div class="container">
</div>

Add some bootstrap into Results.js:
<!-- <div className="row">
    <div className="col-md-12 results">

    </div>
</div> -->

And into Search.js:
<!-- <div className="row">
  <div className="col-md-12">
    <form name="search-form" >
      <div class="form-group">
<label for="exampleInputEmail1">filter results</label>
<input type="text" class="form-control searchbar" id="filter" aria-describedby="emailHelp" placeholder="search"/>
      </div>
    </form>
  </div>
</div> -->



In App.js, import your new components and render them inside your App component

create a constructor function and set states for searchTerm, data results. searchTerm should be an empty string and results and data should be an empty arrays.

pass your states down into your components as props.

Most of the work can be done in App.js and trickled down with props. App.js should pass down a method to Search.js that runs the filter, and Results.js should receive the state of results to be used in its render.

in your src directory, create a file called API to hold our API search and write a method that runs an axios request to the giphy API:
<!-- https://api.giphy.com/v1/gifs/trending?api_key=dc6zaTOxFJmzC&limit=500 -->


In App.js, write a method that calls the state API method and updates the state of data and results on the return

call this method when the component mounts so that we have 500 trending giphys when the page loads.

In App.js, create a method that will receive a searchterm and runs a filter on our data array to filter out any giphys that don't 'include' that term and set the state of results to your new array


In Search.js, create a method that handles any change to the input field and and gets the value of the field.
