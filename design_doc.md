# Design Layout
Looking at the image 
![dashboard-template](dashboard-project.png)
There are three main areas: The dashboard side bar; The header with several buttons and a search bar; the content page-which has two subsections(Projects and Announcments). The general approach will be to use grid to create cells for these main sections. The inner content of each section will either use grid or flex box to separate content.

### Psuedo Code
```html
container for whole body
container for the 3 main sections(dashboard, header, content) 
and sub containter for content for 
projects and announcments/trending
```
```css
grid objects. Dashboard-col:1st 2nd, row:1st last; 
header-col:2nd last, row: first 2nd; 
content-col:2nd last, row:2nd last.
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

## Header
The header consists of a search bar in the upper left hand corner that extends to the middle. Next to it is an
alert bell and avatar with the user name. At the bottom left corner of the header there's the user avatar, a
brief message, and the user name along with their user hangle. To the far right bottom, three bottons occupy the
space: New, Upload, Share.

### Psuedo Code
```html
(header container)>
    div container.search bar>
        input(type='text')
    div conainter.notifacation bell
    div container.user>
        img.user avatar
        span.user name{user name}
    div container.user main>
        img.user avatar main
        p.greet{'Hi, there'}
        span.user name main{User Name}+span.user handle{handle}
    div conainter.buttons>
        button.new+button.upload+button.share
```
