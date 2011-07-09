# Popcorn.capture.js


Create data-uri png posters by capturing any frame in your video!

	var $pop = Popcorn( "#video-id" ),
		poster;

	//	Jump to the frame we want to capture and create a poster!
	poster = $pop.currentTime( 10 ).capture();


	//	Poster will be set by default...
	$pop.currentTime( 10 ).capture();


	//	Teleport, capture and return
	$pop.capture({
		// You can also specify SMPTE time strings
		at: 10
	});


	// Set the captured frame to an image!
	$pop.capture({

		// Any valid selector will work:
		target: "img#capture"
	});


	// Set the captured frame to an image, while returning the
	// popcorn media to continue chaining methods!
	$pop.capture({

		target: "img#capture",

		// Set media:true to override the return!
		media: true

		// This allows us to chain additional methods to this call:
	}).currentTime( 10 ).play();

Jakefile

	jake

		(lone command will run all)

		minify  - UglifyJS on all application code
		hint    - JSHint on all application code
		clean   - delete generated files