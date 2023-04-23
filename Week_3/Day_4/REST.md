## REST
REST is a set of conventions and practices in web development that deals with accessing and manipulating resources over HTTP.

A resource can be an abstraction of an object or data. In practice resources are referenced using a URL (Uniform Resource Locator).

For example, the GitHub API is RESTful. It can be used to manage resources such as Users, Repos, Commits, Gists, and so forth. Each resource can be accessed using an API endpoint (which is simply a URL).

## CRUD -> BREAD

In REST, the notion of Reading is split into two: (1) accessing a whole collection ("Search" or "Browse") and, (2) accessing a single member of that collection. Some developers extend CRUD to include Search, and call it SCRUD. Others think SCRUD is ugly, and instead made up a new mnemonic, BREAD, which stands for: Browse Read Edit Add Delete.

![](/Week_3/Day_4/images/bread.PNG)

## Resource Identifier
When you identify a resource, you must choose a name for it. The name is typically the name of the object type, plural, all lower case, and often with words separated with hyphens (unless it is a singular resource, which we'll get to later). For members of the collection, a unique identifier should be indicated as well. This is done by adding the member object's id after a slash following the collection identifier. For example, the users collection would be identified as /users and the first user would be identified as /users/1.

## Representation

When a resource is transferred (sent back to the user-agent in an HTTP response) it can be in any format and **does not necessarily have to be complete.**

Response should be send in the format Accept header sent in the HTTP request. i.e if Accept header said JSON, response should be JSON format.

![](/Week_3/Day_4/images/respresentation.PNG)

[Click to read about routes - Important](https://web.compass.lighthouselabs.ca/days/w03d4/activities/71)