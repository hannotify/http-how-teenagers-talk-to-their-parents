<!-- .slide: data-background="img/background/teen-not-listening.jpg" data-background-color="black" data-background-opacity="0.4" -->

# Takeaways <!-- .element class="stroke" -->

<https://www.pexels.com/photo/man-scolding-his-son-8550837/> <!-- .element: class="attribution" -->

note:
**Time Elapsed:** `24:30`

---

<table style="font-size: 65%">
    <thead>
        <tr>
            <th>Status Code</th>
            <th>Category</th>
            <th>Teenager Response 🛹💄</th>
        </tr>
    </thead>
    <tbody>
        <tr>
        <!-- <tr class="fragment"> -->
            <td><span class="monospaced">200 OK</span></td>
            <td><span class="badge success">2xx Success</span></td>
            <td>"Yeah, okay."</td>
        </tr>
        <tr>
        <!-- <tr class="fragment"> -->
            <td><span class="monospaced">201 Created</span></td>
            <td><span class="badge success">2xx Success</span></td>
            <td>"I wrote that school report."</td>
        </tr>
        <tr>
        <!-- <tr class="fragment"> -->
            <td><span class="monospaced">202 Accepted</span></td>
            <td><span class="badge success">2xx Success</span></td>
            <td>"Yeah, I'll get to it."</td>
        </tr>
        <tr>
        <!-- <tr class="fragment"> -->
            <td><span class="monospaced">204 No Content</span></td>
            <td><span class="badge success">2xx Success</span></td>
            <td>"Fine!"</td>
        </tr>
        <tr>
        <!-- <tr class="fragment"> -->
            <td><span class="monospaced">304 Not Modified</span></td>
            <td><span class="badge redirection">3xx Redirection</span></td>
            <td>"What did I tell you last time you asked me that?"</td>
        </tr>
        <tr>
        <!-- <tr class="fragment"> -->
            <td><span class="monospaced">400 Bad Request</span></td>
            <td><span class="badge client-error">4xx Client Error</span></td>
            <td>"Well, technically..."</td>
        </tr>
        <tr>
        <!-- <tr class="fragment"> -->
            <td><span class="monospaced">401 Unauthorized</span></td>
            <td><span class="badge client-error">4xx Client Error</span></td>
            <td>"You're not my <em>mum</em> or anything."</td>
        </tr>
        <tr>
        <!-- <tr class="fragment"> -->
            <td><span class="monospaced">403 Forbidden</span></td>
            <td><span class="badge client-error">4xx Client Error</span></td>
            <td>"Dad! You did <em>not</em> just ask me that!"</td>
        </tr>
        <tr>
        <!-- <tr class="fragment"> -->
            <td><span class="monospaced">404 Not Found</span></td>
            <td><span class="badge client-error">4xx Client Error</span></td>
            <td>"I have no idea what you want."</td>
        </tr>
        <tr>
        <!-- <tr class="fragment"> -->
            <td><span class="monospaced">405 Method Not Allowed</span></td>
            <td><span class="badge client-error">4xx Client Error</span></td>
            <td>"That's no way to ask."</td>
        </tr>
        <tr>
        <!-- <tr class="fragment"> -->
            <td><span class="monospaced">418 I'm A Teapot</span></td>
            <td><span class="badge client-error">4xx Client Error</span></td>
            <td>"Enough with the dad jokes already!"</td>
        </tr>
        <tr>
        <!-- <tr class="fragment"> -->
            <td><span class="monospaced">429 Too Many Requests</span></td>
            <td><span class="badge client-error">4xx Client Error</span></td>
            <td>"Stop asking me that."</td>
        </tr>
        <tr>
        <!-- <tr class="fragment"> -->
            <td><span class="monospaced">500 Internal Server Error</span></td>
            <td><span class="badge server-error">5xx Server Error</span></td>
            <td>"(...)"</td>
        </tr>
        <tr>
        <!-- <tr class="fragment"> -->
            <td><span class="monospaced">501 Not Implemented</span></td>
            <td><span class="badge server-error">5xx Server Error</span></td>
            <td>"I don't know how to do that."</td>
        </tr>
        <tr>
        <!-- <tr class="fragment"> -->
            <td><span class="monospaced">503 Service Unavailable</span></td>
            <td><span class="badge server-error">5xx Server Error</span></td>
            <td>"Dad! Can't you see I'm busy?"</td>
        </tr>
    </tbody>
</table>

---

## Why Give More Attention To Status Codes?

<ul>
    <li class="fragment"><strong>Integrations become more reliable</strong> and easier to maintain when APIs use status codes correctly;
    <li class="fragment"><strong>Client-side resilience is improved</strong> as clients can gracefully degrade when encountering status codes <span class="monospaced">503 Service Unavailable</span> or <span class="monospaced">429 Too Many Requests</span>;
    <li class="fragment"><strong>Monitoring and observability reports increase in quality</strong> when APIs use status codes correctly;
    <li class="fragment"><strong>User experience increases</strong> when status codes are interpreted into meaningful feedback for end-users.
</ul>

---

<!-- .slide: data-background="img/background/teen-not-listening.jpg" data-background-color="black" data-background-opacity="0.4" -->

<h1 class="stroke">The Best Way To Learn</h1>
<blockquote class="explanation">
Connect IT concepts to experiences from your personal life&mdash;they will help you to remember.
</blockquote>

note:
And all of this because I thought I saw some kind of pattern when I talked to my kids!

If I have fried your brain with all these status codes and you only have room to remember a single thing, then let it be this:

In my opinion, the best way to learn is to connect IT concepts to experiences from your personal life&mdash;they will help you to remember! And applying these concepts will become so much easier.
