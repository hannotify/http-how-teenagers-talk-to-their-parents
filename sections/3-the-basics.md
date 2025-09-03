<!-- .slide: data-background="img/background/teen-not-listening.jpg" data-background-color="black" data-background-opacity="0.4" -->

# The Basics <!-- .element class="stroke" -->

<https://www.pexels.com/photo/man-scolding-his-son-8550837/> <!-- .element: class="attribution" -->

note:
**Time Elapsed:** `05:00`

---

<!-- .slide: class="basic-http-flow" data-background-size="contain" -->

note:

Almost all software systems that we create today communicate through HTTP, whether they are web applications or REST APIs.
And the HTTP status code are your first line of communication, offering clear insight into what went wrong or right.
So understanding these status codes can save hours of debugging.

---

## Status Code Categories


<table style="font-size: 80%">
    <thead>
        <tr>
            <th>Category</th>
            <th>Purpose</th>
        </tr>
    </thead>
    <tbody>
        <tr class="fragment">
            <td><span class="badge informational">1xx Informational</span></td>
            <td>The request was received, processing continues.</td>
        </tr>
        <tr class="fragment">
            <td><span class="badge success">2xx Success</span></td>
            <td>The request was understood and accepted.</td>
        </tr>
        <tr class="fragment">
            <td><span class="badge redirection">3xx Redirection</span></td>
            <td>The client must take additional action to complete the request.</td>
        </tr>
        <tr class="fragment">
            <td><span class="badge client-error">4xx Client Error</span></td>
            <td>An error occurred, caused by the client.*</td>
        </tr>
        <tr class="fragment">
            <td><span class="badge server-error">5xx Server Error</span></td>
            <td>An error occurred, caused by the server.*</td>
        </tr>
    </tbody>
</table>

<br/>

<small class="fragment">* For all requests apart from <span class="monospaced head">HEAD</span>, the server should include an entity containing an explanation of the error situation, and whether it is temporary or permanent.</small>

note:

As you may know, HTTP status codes fall into different categories: 
(...)

In this talk, we'll primarily focus on the 2xx, 4xx and 5xx categories, as those responses are most common in my experience.
