### fast note taking on data storage in JS

While learning and developing the scroll-meter prototype, one of the basic 'features' I would have liked to have, is continuous counting across browser tabs. Your mileage would then be counted across all the places (tabs) you are scrolling in. This would require storing a simple value somewhere, and calling it again each time the js script runs.

After a bit of research, there seems to be the perfect DOM item to enable this, i.e. *localStorage*. localStorage goes along *sessionStorage* and extremely simply lets you keep up to 5MB of data on the client side, callable (across the entire?) DOM. (Question time: what is a browser tab, technically speaking? Each time I open a new tab, is there a new DOM session opened? Or is the dom like bash maybe? Is there just one DOM, like a processor for the browser, then it just deals with all the rendering of all the tab pages?)

Before considering localStorage,  
