# simple-async
Simple, lightweight and object oriented asynchronous(async) function for javascript

var Async = require('simple-async').simpleAsync;

function test() {
	var promise = new Async();
	
	setTimeout(() => {
		promise.resolve("Have nice day");
	}, 5000);

	return promise.promise;
}

test().then((response) => {
	console.log(response)	
}).catch((err) => {
	console.log(err);
})
