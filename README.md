Step-by-step though process behind the work:

No idea what I'm supposed to do so:

Google accessibility html
W3C-Web Accessibility Initiative (WAI)
    nope (seems a bit too advanced for us)

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
I compared Apple's navigation bar to see if they also used the <ul> tag for their links and they did, so I left the <ul> and <li> tags alone.

Next <div> tag that I looked at was for the class "hero"
    I referenced "https://www.w3schools.com/html/html5_semantic_elements.asp" and wanted to find a tag that would be more specific to an image that they show, and I found that the <figure> tag fit the description (Specifies self-contained content, like illustrations, diagrams, photos, code listings, etc.)
        So I replaced the .hero selector in CSS with the figure selector, and replaced the <div class="hero"> tag with a simple <figure> tag.
            I also noticed in the w3schools link that there is a <figcaption> tag which I realized could be useful for accessibility needs, so I added this tag within the <figure> tag.
                **update**
                Errr the <figcaption> tag was actually not what I expected, it showed in text at the top left corner of the image... So I edited it out for now

Next <div> tag that I looked at was for the class "content", and wanted to find a tag that would be more specific to this box of information filled with text. I found that the <main> tag was most appropriate for this. So I replaced the opening and closing "content" <div> tags in HTML with <main> tags, and replaced the ".content" selector with a "main" selector.

**Rinse and repeat--**
    I replaced the <div> tag for the class "search-engine-optimization" with a <section> tag since it better fit the purpose of this section in my HTML file and replaced all <div> tags within the <main> tab for <section> tags.
        I tried to figure out how to group all <section> tags under the <main> tag since all section selectors in CSS have the same rules (ex. .search-engine-optimization, .online-reputation-management, .social-media-marketing all have the same rules) so I changed all the tags to the same name in HTML to "bluebox" and replaced the first selector in CSS from .search-engine-optimization to .bluebox and deleted the extras (all oline-reputation-management and .social-media-marketing since they all had the same rules apply).
            I used the same concept for the .search-engine-optimization img and replaced it with .bluebox img and deleted the extras (.online-reputation-optimization img and .social-media-marketing img).
   
    Also replaced the <div> tags for "benefits" with <aside> tags:
        (The <aside> tag defines some content aside from the content it is placed in.
        The aside content should be indirectly related to the surrounding content.
        Tip: The <aside> content is often placed as a sidebar in a document.)
    Used the same concept as above with the .bluebox class and did the same for the benefits class, as it also followed all of the same rules in CSS.

Last but not least, replaced "footer" <div> tags with the <footer> element, and also deleted the . from .footer and .footer h2 in the CSS file.

**
I updated the repo directory to replace the original README.md file with this "notes.md" file.
Also adding the screenshot and deployable link at the bottom!
**

![screenshot](./screenshot.png)

https://hak9292.github.io/HTML-CSS-GIT-Code_Refractor/



