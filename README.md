# js-smooth-scroll-devtools
let website scroll smooth from top to footer  

```
(function smoothScrollToBottom() {
    const maxScroll = document.documentElement.scrollHeight - window.innerHeight;
    let currentScroll = window.scrollY || window.pageYOffset;

    // Funktion, um die Seite sanft zu scrollen
    const scrollStep = () => {
        // Ein kleiner Schritt nach unten
        currentScroll += 5;

        // Scrollen, wenn das Ende noch nicht erreicht ist
        if (currentScroll <= maxScroll) {
            window.scrollTo({ top: currentScroll, behavior: 'smooth' });
            // Rekursiver Aufruf für den nächsten Schritt
            requestAnimationFrame(scrollStep);
        }
    };

    // Start des sanften Scroll-Vorgangs
    scrollStep();
})();
```

by change the value from `currentScroll` you can test the scroll-speed  
- open dev-tools
- open console
- copy & paste above script

