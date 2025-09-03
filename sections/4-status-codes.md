<!-- .slide: data-background="img/background/teen-not-listening.jpg" data-background-color="black" data-background-opacity="0.4" -->

# HTTP Status Codes <!-- .element class="stroke" -->

<https://www.pexels.com/photo/man-scolding-his-son-8550837/> <!-- .element: class="attribution" -->

note:
**Time Elapsed:** `06:30`

---

<div class="grid">
    <div class="header">Status Code</div>
    <div><span class="monospaced">200 OK</span></div>
    <div class="header">Category</div>
    <div><span class="badge success">2xx Success</span></div>
    <div class="header">Description</div>
    <div class="span-3">The request was successful.</div>
    <div class="fragment header span-2" data-fragment-index="1">Teenager Response 🛹💄</div>
    <div class="fragment span-2" data-fragment-index="1">"Yeah, okay."</div>
    <div class="fragment header" data-fragment-index="2">Common Use Cases</div>
    <div class="fragment span-3" data-fragment-index="2">
        <ul>
            <li><span class="monospaced get">GET</span>Successful retrieval of at least one resource;
            <li><span class="monospaced post">POST</span>Successful action (that doesn't create a resource);
            <li><span class="monospaced put">PUT</span><span class="monospaced patch">PATCH</span><span class="monospaced delete">DELETE</span>Successful update/deletion of a resource, with a representation of the resource as response body.
        </ul>
    </div>
    <div class="fragment header" data-fragment-index="3">Usage Tips</div>
    <div class="fragment span-3" data-fragment-index="3">
        <ul><li>Use <span class="monospaced">204 No Content</span> instead, if you don't have any content to send.</ul>
    </div>
</div>

---

<div class="grid">
    <div class="header">Status Code</div>
    <div><span class="monospaced">201 Created</span></div>
    <div class="header">Category</div>
    <div><span class="badge success">2xx Success</span></div>
    <div class="header">Description</div>
    <div class="span-3">The request was successful, and a new resource has been created as a result.</div>
    <div class="fragment header span-2" data-fragment-index="1">Teenager Response 🛹💄</div>
    <div class="fragment span-2" data-fragment-index="1">"I wrote that school report."</div>
    <div class="fragment header" data-fragment-index="2">Common Use Cases</div>
    <div class="fragment span-3" data-fragment-index="2">
        <ul>
            <li><span class="monospaced post">POST</span>Successful creation of a new resource;
            <li><span class="monospaced put">PUT</span>Successful creation of a new resource at the specified URI.
        </ul>
    </div>
    <div class="fragment header" data-fragment-index="3">Usage Tips</div>
    <div class="fragment span-3" data-fragment-index="3">
        <ul>
            <li>Make sure to include the <span class="monospaced">Location</span> header in the response;
            <li>For the sake of completeness, also include a representation of the created resource as the response body.
        </ul>
    </div>
</div>

note:
**Time Elapsed:** `07:30`

"This may be hard to believe, but I actually wrote that school report"
"Yes, I actually contributed something to the world today"

---

<!-- .slide: data-auto-animate -->

<pre data-id="201-created"><code class="http" data-trim>
POST /teenager/school-reports HTTP/1.1
Host: hanno.codes
Content-Type: application/json

{
    "title": "The Influence of the Shakespearean Era on Modern-Day Multimedia",
    "author": "Hanno's Kid",
    "subject": "Literature", 
    "content": "(...)"
}
</code></pre>

note:
Here's what that would look like. 

---

<!-- .slide: data-auto-animate -->

<pre data-id="201-created"><code class="http" data-trim>
PUT /teenager/school-reports/2 HTTP/1.1
Host: hanno.codes
Content-Type: application/json

{
    "title": "The Influence of the Shakespearean Era on Modern-Day Multimedia",
    "author": "Hanno's Kid",
    "subject": "Literature", 
    "content": "(...)"
}
</code></pre>

---

## Response

```
HTTP/1.1 201 Created
Location: /teenager/school-reports/2
Content-Type: application/json

{
    "id": 2,
    "title": "The Influence of the Shakespearean Era on Modern-Day Multimedia",
    "author": "Hanno's Kid",
    "subject": "Literature", 
    "content": "(...)"    
}
```

---

<div class="grid">
    <div class="header">Status Code</div>
    <div><span class="monospaced">202 Accepted</span></div>
    <div class="header">Category</div>
    <div><span class="badge success">2xx Success</span></div>
    <div class="header">Description</div>
    <div class="span-3">The request has been accepted for processing, but the processing has not been completed.</div>
    <div class="fragment header span-2" data-fragment-index="1">Teenager Response 🛹💄</div>
    <div class="fragment span-2" data-fragment-index="1">"Yeah, I'll get to it."&nbsp;&nbsp;&nbsp;<small>(but you don't know when)</small></div>
    <div class="fragment header" data-fragment-index="2">Common Use Cases</div>
    <div class="fragment span-3" data-fragment-index="2">
        <ul>
            <li><span class="monospaced post">POST</span>Start a background process, like:
            <ul>
                <li>generating a report;
                <li>sending an e-mail.
            </ul>
            <li><span class="monospaced post">POST</span><span class="monospaced put">PUT</span>Asynchronous creation of a new resource.
        </ul>
    </div>
    <div class="fragment header" data-fragment-index="3">Usage Tips</div>
    <div class="fragment span-3" data-fragment-index="3">
        <ul>
            <li>Include the request's current status in the response, or a URL that points to a status monitor.
        </ul>
    </div>
</div>

note:
**Time Elapsed:** `09:00`

A casual “Yeah, I’ll get to it.”
A promise of future action, often delivered with a tone that suggests it may be indefinitely postponed.
It's a deferral, not a commitment.

---

<!-- .slide: class="accepted-bff" data-background-size="contain" -->

note:

Application of the Backend for Frontend pattern
This approach makes your application more resilient, because when one of the backend systems takes a long(er) time to respond, the frontend experience doesn't suffer.

---

<div class="grid">
    <div class="header">Status Code</div>
    <div><span class="monospaced">204 No Content</span></div>
    <div class="header">Category</div>
    <div><span class="badge success">2xx Success</span></div>
    <div class="header">Description</div>
    <div class="span-3">The server successfully processed the request, but is not returning any content.</div>
    <div class="fragment header span-2" data-fragment-index="1">Teenager Response 🛹💄</div>
    <div class="fragment span-2" data-fragment-index="1">"Fine!"</div>
    <div class="fragment header" data-fragment-index="2">Common Use Cases</div>
    <div class="fragment span-3" data-fragment-index="2">
        <ul>
            <li><span class="monospaced delete">DELETE</span>Successful deletion of a resource;
            <li><span class="monospaced put">PUT</span><span class="monospaced patch">PATCH</span>Successful update of a resource;
            <ul>
                <li>"Save and continue editing" feature for applications like wiki sites.
            </ul>
        </ul>
    </div>
    <div class="fragment header" data-fragment-index="3">Usage Tips</div>
    <div class="fragment span-3" data-fragment-index="3">
        <ul>
            <li>The response can't contain a response body; use <span class="monospaced">200 OK</span> if you've got content to send;
            <li>A <span class="monospaced">204 No Content</span> instructs user agents not to change the render it already has, so don't use it when dealing with queries that yield an empty result. 
            <ul>
                <li>Sending a <span class="monospaced">200 OK</span> with an empty list as response body would be more fitting.
            </ul>
        </ul>
    </div>
</div>

note:
**Time Elapsed:** `11:00`

A short verbal acknowledgment of the request, but with an utter lack of further engagement or information.

---

<div class="grid">
    <div class="header">Status Code</div>
    <div><span class="monospaced">304 Not Modified</span></div>
    <div class="header">Category</div>
    <div><span class="badge redirection">3xx Redirection</span></div>
    <div class="header">Description</div>
    <div class="span-3">The client's cached version of the resource is still valid. The server didn’t need to send a new version.</div>
    <div class="fragment header span-2" data-fragment-index="1">Teenager Response 🛹💄</div>
    <div class="fragment span-2" data-fragment-index="1">"What did I tell you last time you asked me that?"</div>
    <div class="fragment header" data-fragment-index="2">Common Use Cases</div>
    <div class="fragment span-3" data-fragment-index="2">
        <ul>
            <li><span class="monospaced get">GET</span><span class="monospaced head">HEAD</span>Conditional requests 
            <ul><li>should include the <span class="monospaced">If-Modified-Since</span> header field.</ul>
        </ul>
    </div>
    <div class="fragment header" data-fragment-index="3">Usage Tips</div>
    <div class="fragment span-3" data-fragment-index="3">
        <ul>
            <li>Only use when processing the resource is more expensive than determining if the resource has been modified;
            <li>HTTP servers have this functionality baked in for static files (based on the file's timestamp);
            <li>In RESTful API's, consider this for single resources—not for collections.
        </ul>
    </div>
</div>

note:
**Time Elapsed:** `13:00`

"Hi son, you look tired. How about you hit the hay a little earlier today?"
"What did I tell you last time you asked me that?"

---

<div class="grid">
    <div class="header">Status Code</div>
    <div><span class="monospaced">400 Bad Request</span></div>
    <div class="header">Category</div>
    <div><span class="badge client-error">4xx Client Error</span></div>
    <div class="header">Description</div>
    <div class="span-3">The server couldn’t understand the request due to invalid syntax or incorrect parameters.</div>
    <div class="fragment header span-2" data-fragment-index="1">Teenager Response 🛹💄</div>
    <div class="fragment span-2" data-fragment-index="1">"Well, technically..."</div>
    <div class="fragment header" data-fragment-index="2">Common Use Cases</div>
    <div class="fragment span-3" data-fragment-index="2">
        <ul>
            <li>When the request format differs from what the server expected.
        </ul>
    </div>
    <div class="fragment header" data-fragment-index="3">Usage Tips</div>
    <div class="fragment span-3" data-fragment-index="3">
        <ul>
            <li>This should probably be fixed on the client's side;
            <li>On the server: make sure your API is clearly documented.
        </ul>
    </div>
</div>

note:
The default response to anything I ask my daughter.
I talked about this earlier in the talk.

> "Hi angel, can you clean up your room? It looks like a pig stye in there."
> "Well, technically pigs have pointy ears and a curly tail. I have neither of those things, so no, I won't clean up my room."

> "Hi angel, please turn off the TV, you've been watching for over an hour already and we both know that 30 minutes is the limit."
> "Well, technically I watched for 45 minutes yesterday, and you didn't complain about it then. So no, I won't turn off the TV."

Basically, she'll find some loophole in my question that warrants her to dismiss it in its entirety.
It makes me think of legal TV series like “Suits” or “The Lincoln Lawyer” where a mistrial is pronounced whenever a tiny detail in the process is off.
So the request isn’t rejected because it’s impossible to fulfill, but because of a perceived flaw in the _formulation_ of the request itself. 
My teenage kids are actively dissecting and deconstructing my request to escape responsibility.

---

<div class="grid">
    <div class="header">Status Code</div>
    <div><span class="monospaced">401 Unauthorized</span></div>
    <div class="header">Category</div>
    <div><span class="badge client-error">4xx Client Error</span></div>
    <div class="header">Description</div>
    <div class="span-3">The request lacks valid authentication credentials. The client must authenticate itself to get the requested response.</div>
    <div class="fragment header span-2" data-fragment-index="1">Teenager Response 🛹💄</div>
    <div class="fragment span-2" data-fragment-index="1">"You're not my&nbsp;<em>mum</em>&nbsp;or anything."</div>
    <div class="fragment header" data-fragment-index="2">Common Use Cases</div>
    <div class="fragment span-3" data-fragment-index="2">
        <ul>
            <li>Securing endpoints.
        </ul>
    </div>
    <div class="fragment header" data-fragment-index="3">Usage Tips</div>
    <div class="fragment span-3" data-fragment-index="3">
        <ul>
            <li>As a client: are your login credentials or your API key valid?
            <li>This situation is temporary—the server is asking you to try again;
            <li>The name of this status code can be confusing—a better name would be '401 Unauthenticated';
            <li>It should have nothing to do with user permissions (for that, see <span class="monospaced">403 Forbidden</span>).
        </ul>
    </div>
</div>

note:
Me: "Hi sweetheart, do you want me to braid your hair?"
Her, dismissive: "It’s not like you’re my _mum_ or anything." 

– implying that only certain people (e.g., Mum) have the authority to ask that question.

---

<div class="grid">
    <div class="header">Status Code</div>
    <div><span class="monospaced">403 Forbidden</span></div>
    <div class="header">Category</div>
    <div><span class="badge client-error">4xx Client Error</span></div>
    <div class="header">Description</div>
    <div class="span-3">The server understands the request, but refuses to authorize it. Valid authentication credentials may have been provided in the request, but the server considers them insufficient to grant access.</div>
    <div class="fragment header span-2" data-fragment-index="1">Teenager Response 🛹💄</div>
    <div class="fragment span-2" data-fragment-index="1">"Dad! You did&nbsp;<em>not</em>&nbsp;just ask me that!"</div>
    <div class="fragment header" data-fragment-index="2">Common Use Cases</div>
    <div class="fragment span-3" data-fragment-index="2">
        <ul>
            <li>Restricting endpoint access to the set of users that have the right permissions;
            <ul><li>For example, when a regular website user tries to access an administrator endpoint.</ul>
        </ul>
    </div>
    <div class="fragment header" data-fragment-index="3">Usage Tips</div>
    <div class="fragment span-3" data-fragment-index="3">
        <ul>
            <li>As a client: check the permissions that were granted to you;
            <li>This situation is probably permanent;
            <li>It should have nothing to do with failed login attempts (for that, see <span class="monospaced">401 Unauthorized</span>).
        </ul>
    </div>
</div>

note:
If it was up to my daughter, it would be called “403 Disgusted”. “Dad! You did _not_ just ask me that!”
A defensive “Dad! You did _not_ just ask me that!” – a clear boundary violation and a strong rejection of the inquiry.
Heard regularly when asking my teenage son about his love interests.

---

## 401 vs. 403

<span class="monospaced">401 Unauthorized</span> means "You need to log in first",
which makes it an <em>identity issue</em>.

<p class="fragment">
    <span class="monospaced">403 Forbidden</span> means "You're logged in, but you're not allowed to do that",
    which makes it a <em>permission issue</em>.
</p>

---

<!-- .slide: data-background="img/jcon-403-dark.jpg" data-background-size="contain" -->

---

<div class="grid"> 
    <div class="header">Status Code</div>
    <div><span class="monospaced">404 Not Found</span></div>
    <div class="header">Category</div>
    <div><span class="badge client-error">4xx Client Error</span></div>
    <div class="header">Description</div>
    <div class="span-3">The server can't find the requested resource.</div>
    <div class="fragment header span-2" data-fragment-index="1">Teenager Response 🛹💄</div>
    <div class="fragment span-2" data-fragment-index="1">"I have no idea what you want."</div>
    <div class="fragment header" data-fragment-index="2">Common Use Cases</div>
    <div class="fragment span-3" data-fragment-index="2">
        <ul>
            <li>Broken links;
            <li>A particular resource doesn't exist (yet).
        </ul>
    </div>
    <div class="fragment header" data-fragment-index="3">Usage Tips</div>
    <div class="fragment span-3" data-fragment-index="3">
        <ul>
            <li>As a client, did you use the right URI?
            <li>On the server, avoid using identifiers that can be easily guessed;
            <li>If you're sure the resource will be missing for good, use <span class="monospaced">410 Gone</span> instead.
        </ul>
    </div>
</div>

note:
A blank stare and "I have no idea what you want." – denial of knowledge or responsibility.
The requested information (or chore) simply doesn’t exist in their realm of awareness.

---

<div class="grid"> 
    <div class="header">Status Code</div>
    <div><span class="monospaced">405 Method Not Allowed</span></div>
    <div class="header">Category</div>
    <div><span class="badge client-error">4xx Client Error</span></div>
    <div class="header">Description</div>
    <div class="span-3">The server understands the request, but the HTTP method is not allowed for that resource.</div>
    <div class="fragment header span-2" data-fragment-index="1">Teenager Response 🛹💄</div>
    <div class="fragment span-2" data-fragment-index="1">"That's no way to ask."</div>
    <div class="fragment header" data-fragment-index="2">Usage Tips</div>
    <div class="fragment span-3" data-fragment-index="2">
        <ul>
            <li>As a client, check if you're using the right HTTP method;
            <li>On the server, include an <span class="monospaced">Allow</span> response header that contains a list of the target resource's supported methods.
        </ul>
    </div>
</div>

note:
A disgusted “That's no way to ask.” – A rejection of the request as fundamentally inappropriate or unconventional. It’s not a matter of _can't_ do it, but _won’t_ do it because it’s strange.
The request itself isn’t incomprehensible, but the way you’re asking it (the "method") is unacceptable. It’s a judgment on the approach, not the request itself.

This exchange used to be the other way around, when my kids were younger.

---

<div class="grid"> 
    <div class="header">Status Code</div>
    <div><span class="monospaced">418 I'm A Teapot</span></div>
    <div class="header">Category</div>
    <div><span class="badge client-error">4xx Client Error</span></div>
    <div class="header">Description</div>
    <div class="span-3">The server refuses to brew coffee because it is a teapot.</div>
    <div class="fragment header span-2" data-fragment-index="1">Teenager Response 🛹💄</div>
    <div class="fragment span-2" data-fragment-index="1">"Enough with the dad jokes already!"</div>
    <div class="fragment header" data-fragment-index="2">Common Use Cases</div>
    <div class="fragment span-3" data-fragment-index="2">
        <ul>
            <li>It made a fine April Fools joke back in 1998;
            <ul><li><a href="https://www.rfc-editor.org/rfc/rfc2324">rfc-editor.org/rfc/rfc2324</a></ul>
            <li>Some websites use this response for requests they do not wish to handle, such as automated queries, and other people use it for debugging purposes;
            <li>Also, Google uses it: <a href="https://www.google.com/teapot">google.com/teapot</a>;
            <li>...but that doesn't mean you should!
    </div>
</div>


---

<div class="grid"> 
    <div class="header">Status Code</div>
    <div><span class="monospaced">429 Too Many Requests</span></div>
    <div class="header">Category</div>
    <div><span class="badge client-error">4xx Client Error</span></div>
    <div class="header">Description</div>
    <div class="span-3">The user has sent too many requests in a given amount of time.</div>
    <div class="fragment header span-2" data-fragment-index="1">Teenager Response 🛹💄</div>
    <div class="fragment span-2" data-fragment-index="1">"Stop asking me that."</div>
    <div class="fragment header" data-fragment-index="2">Common Use Cases</div>
    <div class="fragment span-3" data-fragment-index="2">
        <ul>
            <li>Rate limiting.
        </ul>
    </div>
    <div class="fragment header" data-fragment-index="3">Usage Tips</div>
    <div class="fragment span-3" data-fragment-index="3">
        <ul>
            <li>Include a <span class="monospaced">Retry-After</span> header that indicates how long a client should wait before making the request again.
            <li>If the problem isn't related to a particular client but rather occurring for all clients, use <span class="monospaced">503 Service Unavailable</span> instead.
        </ul>
    </div>
</div>

note:
A clear indication that the request frequency is overwhelming, and further inquiries are unwelcome.
It captures the essence of rate limiting – the request itself isn't invalid, but the sheer volume is causing a problem. It's a plea for space and a break from constant questioning.

This exchange used to also be the other way around, when my kids were younger.

---

<div class="grid"> 
    <div class="header">Status Code</div>
    <div><span class="monospaced">500 Internal Server Error</span></div>
    <div class="header">Category</div>
    <div><span class="badge server-error">5xx Server Error</span></div>
    <div class="header">Description</div>
    <div class="span-3">The server encountered an unexpected condition that prevented it from fulfilling the request.</div>
    <div class="fragment header span-2" data-fragment-index="1">Teenager Response 🛹💄</div>
    <div class="fragment span-2" data-fragment-index="1">"(...)"</div>
    <div class="fragment header" data-fragment-index="2">Common Use Cases</div>
    <div class="fragment span-3" data-fragment-index="2">
        <ul>
            <li>A generic 'catch-all' response to server issues;
            <li>Only meant to be used when the server cannot find a more appropriate 5xx error to respond with.
        </ul>
    </div>
    <div class="fragment header" data-fragment-index="3">Usage Tips</div>
    <div class="fragment span-3" data-fragment-index="3">
        <ul>
            <li>There can be many possible causes, such as:
            <ul style="font-size: 0.75em">
                <li>improper server configuration;
                <li>out-of-memory issues;
                <li>unhandled exceptions;
                <li>improper file permissions, etc.
            </ul>
            <li>Include details on the error that occurred in the response;
            <li>Make sure to log all 500 errors in a detailed way, so you can improve the stability of your services in the future.
        </ul>
    </div>
</div>

note:
The default response to anything I ask my son.
I talked about this earlier in the talk.

> Dad: *asks kid to do a chore*
> Kid: (…)
> Dad: “Hello?”
> Kid: (…)
> Dad (getting impatient): “Hellooo?! Earth to kid?!”
> Kid: "What? I didn't hear you..."

Because if you don't answer, you may just get off the hook!

---

<div class="grid"> 
    <div class="header">Status Code</div>
    <div><span class="monospaced">501 Not Implemented</span></div>
    <div class="header">Category</div>
    <div><span class="badge client-error">5xx Server Error</span></div>
    <div class="header">Description</div>
    <div class="span-3">The server does not support the functionality to fulfill the request.</div>
    <div class="fragment header span-2" data-fragment-index="1">Teenager Response 🛹💄</div>
    <div class="fragment span-2" data-fragment-index="1">"I don't know how to do that."</div>
    <div class="fragment header" data-fragment-index="2">Common Use Cases</div>
    <div class="fragment span-3" data-fragment-index="2">
    <ul>
        <li>The server does not recognize the request method and is incapable of supporting it. 
    </ul>
    </div>
    <div class="fragment header" data-fragment-index="3">Usage Tips</div>
    <div class="fragment span-3" data-fragment-index="3">
        <ul> 
            <li>Servers are required to support <span class="monospaced get">GET</span> and <span class="monospaced head">HEAD</span>, and so they can't return a 501 on requests that use these methods.
            <li>If the method is recognized but not allowed by the server, the appropriate response is <span class="monospaced">405 Method Not Allowed</span>.
            <li>If the user has hit an unimplemented API that may be available at a later point in time, use <span class="monospaced">404 Not Found</span> or <span class="monospaced">503 Service Unavailable</span> instead.
        </ul>
    </div>
</div>

note:
Dad: “Time to get up, kid. You've got school in 45 minutes.”.
Teenager: ”(...)&nbsp;&nbsp;😴" *feigned sleeping*
But if he was able to talk, he'd say: "I don't know how to do that."

Absolute non-compliance, often accompanied by feigned sleep or a complete lack of acknowledgement. The functionality (waking up early) is simply not implemented in their operating system.

Usage Tips: probably never use, as this status code is only appropriate when the HTTP method is unknown (PARTY request)

---

<div class="grid"> 
    <div class="header">Status Code</div>
    <div><span class="monospaced">503 Service Unavailable</span></div>
    <div class="header">Category</div>
    <div><span class="badge client-error">5xx Server Error</span></div>
    <div class="header">Description</div>
    <div class="span-3">The server is temporarily unavailable.</div>
    <div class="fragment header span-2" data-fragment-index="1">Teenager Response 🛹💄</div>
    <div class="fragment span-2" data-fragment-index="1">"Dad! Can't you see I'm busy?"</div>
    <div class="fragment header" data-fragment-index="2">Common Use Cases</div>
    <div class="fragment span-3" data-fragment-index="2">
        <ul>
            <li>Appropriate when a server is down for maintenance or overloaded.
        </ul>
    </div>
    <div class="fragment header" data-fragment-index="3">Usage Tips</div>
    <div class="fragment span-3" data-fragment-index="3">
        <ul>
            <li>Include a <span class="monospaced">Retry-After</span> header that indicates how long a client should wait before making the request again;
            <li>Include a user-friendly response body that explains the problem in more detail;
            <li>A 503 means the problem is temporary. For permanent problems, use <span class="monospaced">500 Internal Server Error</span> instead;
            <li>If requests from specific clients are being restricted, use <span class="monospaced">429 Too Many Requests</span> instead.
        </ul>
    </div>
</div>

note:
"Dad! Can't you see I'm busy?"
An abrupt dismissal, often with no indication of _what_ they’re busy with (but probably with their phone).
