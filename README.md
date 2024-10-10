# Keep Talking and Everybody Codes

A repository to show how you write code and think about it.
A starting point for a good discussion about our job!

## Context

You probably came here because you have a second interview with us.
In a meeting like that we would like to talk more about technology.
We want to see how you write code, how you think and what you think is important when writing code.
In short: we want to kickstart our discussion about code.

There's multiple ways to do this.
Perhaps you have open source projects you'd like to show us.
Maybe you have a previous project of which you can share the code.
And that's fine with us.
But perhaps you don't have that (yet).
That's where this repository comes in: a starting point to write some code as a good basis for a discussion about technology!

"Is this a _test_?" you might be asking?
The answer is very clear: **no**!
_It does look a little like a test_ (and that's intentional!), but there's some important differences:

- It doesn't determine whether you will be invited (okay, unless you do something _really_ weird). We already decided you could come back before we sent you here. So you'll always get the chance to explain your choices.
- We want you to **timebox this to 2 to 4 hours**. It makes sense if you don't get to finish everything in that time. Focus on showing what you think is important, and explain those choices to us.
- With a 'test' you can succeed or fail, or you get a grade. This is just _input_ for our next meeting.

## The Exercise

The exercise consists of three parts where you use the dataset you'll find in [data/cameras-defb.csv](data/cameras-defb.csv).
This is a set of camera data from the Dutch city of [Utrecht](https://en.wikipedia.org/wiki/Utrecht).
You can do the exercise in a language and stack of your choosing (we are mostly familiar with C#, JavaScript, TypeScript, PHP, Python).

## CLI

Make a program or script that allows the user to search via the CLI for part of a camera _name_, like:

```sh
# Calling PHP via the CLI
php search.php --name Neude

# Or if you used .NET:
dotnet Search --name Neude

# Etc.
```

Expected output:

```none
501 | UTR-CM-501 Neude rijbaan voor Postkantoor | 52.093421 | 5.118278
503 | UTR-CM-503 Neude plein | 52.093448 | 5.118536
504 | UTR-CM-504 Neude / Schoutenstraat | 52.092995 | 5.119088
505 | UTR-CM-505 Neude / Drakenburgstraat / Vinkenurgstraat | 52.092843 | 5.118351
506 | UTR-CM-506 Vinkenburgstraat / Neude | 52.092378 | 5.117902
507 | UTR-CM-507 Vinkenburgstraat richting Neude | 52.092234 | 5.117766
etc.
```

## API

Serve the data from the csv from a REST API, such that a web application can fetch that data.

## Web application

For the frontend you can choose whether or not to use a framework, and if so, which framework.
Think about what you want to show and what you want to talk about in the technical meeting.

### Page with data table

The first part of the frontend consists of fetching the data from the API.
Show the data spread across five columns on the homepage of the application.
_Optionally_ you can use [code/index.html](https://github.com/infi-nl/everybody-codes/blob/main/code/index.html) as a starting point.
The data should be spread according to the following rules, based on the _number_ of the camera:

1. Column with cameras with numbers up to 600.
2. Column with cameras with numbers 600 to 700.
3. Column with cameras with numbers 700 to 800.
4. All other camera's

### Plot map with cameras

The second part is about showing the cameras as markers on a map.
Show _all_ cameras as markers on a map of Utrecht, above the table with camera data.
The optional setup in [code/index.html](https://github.com/infi-nl/everybody-codes/blob/main/code/index.html) gives an indication of how this should look.

You can use a map tool of choice.
If you don't have a preference you could [use the quick start of Leaflet](https://leafletjs.com/examples/quick-start/).
The library suggests that you use OpenStreetMaps, which works fine for this exercise, and at the time of writing this doesn't require a complicated signup with a credit card.

Tip: [coordinates 52.0914 to 5.1115 are centered on Utrecht](https://www.openstreetmap.org/#map=14/52.0914/5.1115).

## About the title

Huh?

> Keep Talking and Everybody Codes

"_What's that?_"
Sorry, it's a pun related to [a fun game](http://www.keeptalkinggame.com/).

## License en Copyright

See [LICENSE.txt](LICENSE.txt) for complete details. This fork was translated from the original by [Infi](https://github.com/infi-nl/everybody-codes).
