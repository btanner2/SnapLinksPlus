# Next Minor Release (3.1.1)
 - **Bugs**
    - Escape Key on https://thirteenag.github.io/wfp is not being stopped

 - **Features**
    - Add &lt;button> as clickable type
    - Signing of beta versions for wider testing

 - **Test, issue?**
    - Possible improvement to obscured element detection:
        - Use the middle point of the intersection of the selection rect and the bounding rect
            rather than the middle point of the bounding rect, this catches cases where the bottom
            half of the element is obscured, but not all of it

     - Consider: querySelectorAll('*:enabled') may give all elements of concern, even Elements which are divs but have an onclick() enabled or listened to.


 -  **Todo**
    - Switch this._onKeyUp = ... .bind() to this.onKeyUp = ... .bind()

# Next Major Release (3.2.0)
 - **Bugs**
    -

 - **Features**
    - Options GUI (minimal)

 - **Test, issue?**
    -


# Known Bugs


# Plans
 - Create Updated Plugin Page
 - Setup site using Jekyll
 - Add Options GUI
 - Better handling of label placement (separate from sizing rect, above &lt;SVG> Element)
 - Highlight "greatest of types" elements differently than elements which do not meet the greatest of.
    eg: 3 Buttons and 1 Anchor lassoed, the 3 Buttons would be highlighted in green vs the Anchor being highlighted in grey


# Todo / Ideas
 - Mutation Observer (clear DocElemRects, re-index if during drag)
 - Resolve all inspection errors
 - Externalize CSS Styles
 - Compiler/minimizer for production build?
 - docElem is a sandboxed global, replace document.documentElement references with docElem
 - Update phing (if js-csp/transducers.js work out)
    - js-csp
        - npm install
        - copy csp.min.js to src/lib
    - transducers.js
        - download/install (npm?)
        - copy transducers.js to src/lib
- Refactor ElemDocRects / RectMapper to ElemCache/ElemCacher (to reflect new font-size cache functionality)

# Test
 -

# Deferred / Possibly Won't Implement
 - Add Elements that have cursor: pointer (and have a click handler?)

# Feature Requests
 - [Issue #91](https://github.com/cpriest/SnapLinksPlus/issues/91)-1 - Width of selection box independent of zoom factor... possibly doable with SVG since it has it's own coordinate system??

<style>
    del { opacity: .5; }
    A { color: #36a3d9; text-decoration: underline; }
    BODY { background-color: black; }
    ARTICLE.markdown-body { padding: 35px !important; background-color: #1a1817 !important; }

/*  span { position: relative; }
    del::after {
        border-bottom: 1px solid rgba(255,255,255,.4);
        content: "";
        left: 0;
        position: absolute;
        right: 0;
        top: 50%;
    } */
</style>
