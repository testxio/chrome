# A Docker image of Chrome for headless testing
To be used with [testx](http://testx.io/testx).

## Dependencies
Make sure you have all required dependencies locally.
With [testx](http://testx.io/testx) you'll need at least [Protractor](http://www.protractortest.org) and possibly [CoffeeScript](http://coffeescript.org/) (for [testx](http://testx.io/testx) 2.x).

## Usage
The entry point of the image is `npm test`, so this:
```bash
docker run -it --rm -v $(pwd):/work testx/chrome
```
will execute `npm test` in the container.

You can parameterize the execution just like you would an npm run.
For example:
```bash
docker run -it --rm -v $(pwd):/work testx/chrome -- --baseUrl=http://localhost:3000
```
will execute tests against http://localhost:3000, assuming `npm test` runs  [Protractor](http://www.protractortest.org).
