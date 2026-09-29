# SI 539 Week 9: Midterm Prep

Today is all hands-on-keyboard. You'll build a layout from scratch the way you will on the midterm, level by level.

| Part | What | Time |
|---|---|---|
| 1 | Build It (solo, exam conditions) | 35 min |
| 2 | Review + cheat sheet | 10 min |

> **Exam rules:** open notes, open internet, **no AI, no classmates.** Treat it like the real thing.

**Efficiency counts on the midterm.** Delete or comment out any code you don't need.

---

## Build It

Open `index.html` with Live Server. Write all your CSS in `css/style.css`. **Do not edit the HTML.**

Each level has a time box that roughly matches midterm pacing. If you're stuck when time runs out, leave a comment and move on, just like on the exam.

### Level 1: Skip link (4 min)

1. "Skip to Main Content" is **hidden** when the page loads.
2. It **appears** when a visitor presses **Tab** for the first time.

| On load | After pressing Tab |
|---|---|
| ![skip link hidden](screenshots/skip-hidden.png) | ![skip link visible](screenshots/skip-focused.png) |

✅ **Check:** Reload, press Tab once. Does the link appear? Tab again. Does it go away?

### Level 2: Grid container, `.first` (5 min)

1. Grid with **3 equal columns of 25% each**
2. **3px** solid border, color **#e91e63**
3. **50px** gap between columns and rows

### Level 3: Grid children (6 min)

Default styles for every child of `.first`:

1. **3px dashed** border, color **#7332a8**
2. A gray background of your choice
3. Rounded corners (about 15px)
4. **45px** padding on top and bottom, **20px** on the sides
5. Centered text

### Level 4: The last element (3 min)

The **final element** spans **all columns**, and its corners are **not rounded**.
Use **1 selector** and **2–3 declarations** at most.

### Level 5: `:nth-child` (4 min)

Give the items in the **middle column** (**B, E and H**) a **white** background.

- Use **one** `:nth-child()` selector. Don't list B, E and H separately.
- J should stay gray.

💡 **Hint:** Write out the position numbers of B, E and H. What's the pattern? `:nth-child()` accepts formulas like `an + b`.

### Level 6: `:hover` (3 min)

When the mouse is over **any** grid item, its background turns **#7332a8** and its text turns **white**.

![hover state on E](screenshots/hover.png)

✅ **Check:** Hover over **B, E and H** too. Do they turn purple? If not, look at the **order** of your rules and compare their specificity.

### Level 7: Image (5 min)

The page has a banner image (`.banner`) above the grid.

1. The image fills the **full width** of the page.
2. It's **200px** tall **without being stretched or squished**.
3. Rounded corners (about 15px)
4. **20px** of space between the image and the grid

💡 **Hint:** Setting both a width and a height distorts an image. Which property crops it instead?

**Target: mobile view at 700px wide** (Levels 1–7)

![mobile view](screenshots/mobile-700.png)

✅ **Check:** Resize the window. Does the image stay the full width without squishing?

### Level 8: Desktop breakpoint (5 min)

Inside a media query. **No `max-width` allowed.**

1. Breakpoint at **800px**
2. Container background becomes **#bdd4fc**
3. Center all grid items **by adding to the grid container**
4. The banner image becomes **300px** tall

**Target: desktop view at 1000px wide**

![desktop view](screenshots/desktop-1000.png)

🔎 **Use DevTools:** In the Elements panel, click the **`grid`** badge next to `<div class="first">` to turn on the grid overlay. Try `justify-items` and `align-items` values live in the Styles pane before writing them in your file. To test hover without the mouse, right-click an element and choose **Force state → :hover**.

### ⭐ Bonus

What's the difference between `justify-content` and `justify-items`? Try both in DevTools, then explain it in a comment at the bottom of `style.css`.

---

## Review + Cheat Sheet

Add one line to your cheat sheet for anything you had to look up today. Good things to have on hand:

- Skip link pattern (hide and show on `:focus`)
- `grid-template-columns`, `repeat()`, `gap`, `grid-column: 1 / -1`
- `:nth-child()` formulas: `odd`, `even`, `3n`, `3n + 1`, `3n + 2`
- `:hover`, and why rule order matters when specificity ties
- Image sizing: `width: 100%`, `object-fit: cover`
- Shorthand order for `padding` and `border`
- `@media (min-width: ...)` template

**Submit:** Upload your `style.css` to Canvas.
