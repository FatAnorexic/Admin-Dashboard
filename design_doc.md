# Design Layout
Looking at the image 
![dashboard-template](dashboard-project.png)
There are three main areas: The dashboard side bar; The header with several buttons and a search bar; the content page-which has two subsections(Projects and Announcments). The general approach will be to use grid to create cells for these main sections. The inner content of each section will either use grid or flex box to separate content.

### Psuedo Code
```html
container for whole body
container for the 3 main sections(dashboard, header, content) and sub containter for content for projects and announcments/trending
```
```css
grid objects. Dashboard-col:1st 2nd, row:1st last; header-col:2nd last, row: first 2nd; content-col:2nd last, row:2nd last.
```

---

## Dashboard

The dashboard consists of 9 objects, and there is a very visible gap bewteen the first 6 and last 3. 

### psuedo code

```html
div container for whole dash board
    unorded list of links to:
        home, profile, messages, history, tasks,
        communities, settings, support, privacy
```
```css
container is grid object extending from the first
column to the second, and from the first row down to
the last

background color is light blue(grade against image to match)
text is white, and font needs is different from rest of document.
```