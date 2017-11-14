footer: CSS Grid Meetup, Nov. 2017
build-lists: true

# [fit] CSS Grid Meetup

## Aarhus, November 2017

---

# CSS Grid

![](examples/css_track_1024.png)

---

# [fit] Basics

---

## Basics

![fit right](examples/rows-columns-gaps.png)

* Container
* Rækker (rows)
* Kolonner (columns)
* Mellemrum (gap)

---

## Basics

```less
ul {
  display: grid;
}
```

---

## Basics

```less
ul {
  display: grid;
  grid-template-rows: 200px 200px 200px;
}
```

---

## Basics

```less
ul {
  display: grid;
  grid-template-rows: 200px 200px 200px;
  grid-template-columns: 200px 200px 200px;
}
```

---

## Basics

```less
ul {
  display: grid;
  grid-template-rows: 200px 200px 200px;
  grid-template-columns: 200px 200px 200px;
  grid-gap: 10px;
}
```

^ Der er heldigvis en funktion til repeating cols/rows

---

## Basics

```less, [.highlight: 3,4]
ul {
  display: grid;
  grid-template-rows: repeat(3, 200px);
  grid-template-columns: repeat(3, 200px);
  grid-gap: 10px;
}
```

---

> **“Lad os da lige prøve…”**

^ examples/basics-start.html

---

# [fit] Advanced

---

# Ny CSS unit: `fr`(action)

```less
grid-template-columns: 2fr 1fr 3fr;
```

---

> **“Lad os da lige prøve det også…”**

^ examples/advanced-start.html

---

# [fit] Fallback

---

# [fit] `@supports()`

---

```less
.page {
  display: grid;
  grid-template-columns: repeat(3, 200px);
}
```

# :arrow_double_down:

```less, [.highlight: 1,6]
@supports(display: grid) {
  .page {
    display: grid;
    grid-template-columns: repeat(3, 200px);
  }
}
```

^ Hvis `grid` er supporteret, er `@supports()` også!