<!-- .slide: data-background="img/background/teen-not-listening.jpg" data-background-color="black" data-background-opacity="0.4" -->

# HTTP Status Codes <!-- .element class="stroke" -->

<https://www.pexels.com/photo/man-scolding-his-son-8550837/> <!-- .element: class="attribution" -->

---

<div class="grid">
    <div class="header">Status Code</div>
    <div><span class="monospaced">200 OK</span></div>
    <div class="header">Category</div>
    <div><span class="badge success">2xx Successful</span></div>
    <div class="header">Description</div>
    <div class="span-3">The request was successful.</div>
    <div class="header span-2">Mysterious Teenager Response 🛹</div>
    <div class="span-2">"Yeah, okay."</div>
    <div class="header">Common Use Cases</div>
    <div class="span-3">
        <ul>
            <li><span class="monospaced get">GET</span>Successful retrieval of at least one resource.
            <li><span class="monospaced put">PUT</span><span class="monospaced patch">PATCH</span>Successful update of a resource.
            <li><span class="monospaced post">POST</span>Successful action (that doesn't create a resource).
            <li><span class="monospaced delete">DELETE</span>Successful deletion of a resource (alternatively <span class="monospaced">204 No Content</span>)
        </ul>
    </div>
</div>

---

<div class="grid">
    <div class="header">Status Code</div>
    <div class="monospaced">404 Not Found</div>
    <div class="header">Category</div>
    <div><span class="badge clientError">4xx Client Error</span></div>
    <div class="header">Description</div>
    <div class="span-3">Lorum ipsum dolor sit amet</div>
    <div class="header span-2">Mysterious Teenager Response 🛹</div>
    <div class="span-2">"Bruh!"</div>
    <div class="header">Common Use Cases</div>
    <div class="span-3">
        <ul>
            <li>A resource doesn't exist;
            <li>A webpage has been removed;
            <li>A developer was being lazy.
        </ul>
    </div>
    <div class="header">Troubleshooting Tips</div>
    <div class="span-3">...only for error codes</div>
</div>

