### fast note taking on data storage in JS

While learning and developing the scroll-meter prototype, one of the basic 'features' I would have liked to have, is continuous counting across browser tabs. Your mileage would then be counted across all the places (tabs) you are scrolling in. This would require storing a simple value somewhere, and calling it again each time the js script runs.

After a bit of research, there seems to be the perfect DOM item to enable this, i.e. *localStorage*. localStorage goes along *sessionStorage* and extremely simply lets you keep up to 5MB of data on the client side, callable (across the entire?) DOM. (Question time: what is a browser tab, technically speaking? Each time I open a new tab, is there a new DOM session opened? Or is the dom like bash maybe? Is there just one DOM, like a processor for the browser, then it just deals with all the rendering of all the tab pages?)

Before considering localStorage, cookies were what seemed to be the best suited. I found out quickly though that cookies can only be set and updated on GET and POST requests (exclusively those, or maybe any traffic? I think they are the main ones anyway). The value I'm trying to store across tabs is a simple integer, but it gets updated on an event trigger in JS, a scolling event. So it gets update a lot. And making a post event each time the event is triggered I think could be possible, technically speaking, but I don't think the browser would be very happy with firing possibly hundreds of posts in rapid sequence.

The issue is that localStorage is domain specific. This means that I can store values but the value does not port over between different websites, which makes the entire thing quite useless, and back to square one.

Unless, I managed, externally, to collect each value from each tab, and just add them up? I think that could be possible, I think you can get different tab values? w1.localStorage.prevCumulativeDist something like this?

Oh, also, last night I tried to push my commits, but ran into the weirdest error: apparently my permissions were too loose on my .ssh folder contents? Git was refusing to let me push because 'anyone' could read my key. Something happened between my last and second last push yesterday to my permissions. I don't know how it happened. Kind of scary? I did leave my computer in the studio, while I went out to meet people, but who would creep up to my computer like that? Hum...

Ok go.
