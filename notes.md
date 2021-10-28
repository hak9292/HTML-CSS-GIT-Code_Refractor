No idea what I'm supposed to do so:

Google accessibility html
W3C-Web Accessibility Initiative (WAI)
    nope (seems a bit advanced)

Google: "accessibility elements html"
https://developer.mozilla.org/en-US/docs/Learn/Accessibility/HTML
    ***Using SEMANTICS is important!!!***
    ex. <div>Play video</div>
        vs.
        <button>Play video</button>
        Screen reader?...

ChromeVox
    Ctrl + Alt + z (Shortcut if using the chrome extension)
    Messed around with it and every section that I hovered my mouse over would tell me what part of the page I was pointing at--I could see it being very useful for those who are visually impaired

HTML Role attribute--describes the role of an element in programs that can make use of it, such as screen readers or magnifiers.
Usage Example:
    <a href="#" role="button">Button Link</a>

**First Steps**
Taking a first look, header class should be its own tag, so I cmd + / the <div class="header"> opening and closing tags and inserted my own header tags where the header class used to be.
I then went over to the style.css file and removed the "." in front of all the .header selectors and the page remained the same (***Began to understand more clearly what they wanted from this assignment--you have to make it more "accessible" in the sense that the semantics have to be better (more specific) while the page remains the same visually, so by the time you replace a lot of the tags in HTML 

Googled <span> tag, and it says "A <span> element which is used to color a part of a text:
    So I realized that the "seo" in Horiseon wasn't separated for no reason

**Second Steps**
Honestly should have been my first step... I wanted to look at some of the biggest websites that would most likely have some good references, so I went to "https://www.apple.com/" and inspected the element to see which semantics they use for their website
    I wanted to run down the index.html page (from our HW) in chronological order, and the first <div> tag I ran into is the div tag listing the navigation links (ex. Search Engine Optimization, Online Reputation Management) and looked at Apple and saw that they used <nav> tags, so I replaced the <div> tags in the HTML file with the <nav> tag (ex. header div ul-->header nav ul)
