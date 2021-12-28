# crawler - A DSL for web crawling in Scala

The purpose of this project is to provide a nice DSL wrapper around the
cumbersome htmlunit Java library.  Here is an example taken from a unit 
test in this package:

This `TestCrawler` class defines a crawl that will navigate to google, 
find the form whose id is `tsf`, type something into the form, then
click on the submit button named `btnK`, which will then take us to a 
new page (the search results) where we can then grab the content of the
`resultStats` div.

It also grabs URL from a link defined by XPath and downloads it to given
OutputStream.

Alternatively you could just get bytes instead of writing downloaded data to 
OutputStream: `download(url).getBytes`.

