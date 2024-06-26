# Design Layout
Looking at the image 
![dashboard-template](dashboard-project.png)
There are three main areas: The dashboard side bar; The header with several buttons and a search bar; the content page-which has two subsections(Projects and Announcments). The general approach will be to use grid to create cells for these main sections. The inner content of each section will either use grid or flex box to separate content.

A mathjax script is imported into the head, as a means to display math symbols on the page. 

### Psuedo Code
```html
body>
    div.header#header
    div.sidebar#sidbar
    div.content#content
```
```css
body{
    min-height 100vh /*This makes the grid fill the entire view port*/
    display grid
    margin 0
    grid template area: min-content 4fr/1fr 4fr
    fonts
}

sidebar{
    background->#287292
    grid area 1/1/-1/2
    display grid rows min min
    margin 0
}
header{
    grid area 1/2/2/4
    display inline-grid min min /2fr auto
    background #FAF9F6
    padding 
    box-shadow
}
content{
    background->grayish
    grid area 2/2/4/-1
}
```

---

## Dashboard

The dashboard consists of 9 objects, and there is a very visible gap bewteen the first 6 and last 3.
The top of the dashboard section contains the logo along with an image for it.
The unordered list is as follows: Home, profile, messages, history, tasks, communities, <'visible gap'>,
settings, suppot, privacy.


### psuedo code

```html
div.sidebar#sidebar>
    div.logo>
        img.icon+div.items#dashboard
    ul.itmes>li.(class name){object name}*6
    ul.items.secondary>li.second{objectname}*3
```
```css
sidebar, content, header{
    border(temporaray)
    text align
}

sidebar{
    background->light blue
    grid area 1/1/-1/2
    display grid
    grid tracks min-content
}
```

---

## Header
The header consists of a search bar in the upper left hand corner that extends to the middle. Next to it is an
alert bell and avatar with the user name. At the bottom left corner of the header there's the user avatar, a
brief message, and the user name along with their user hangle. To the far right bottom, three bottons occupy the
space: New, Upload, Share.

### Psuedo Code
```html
(header)>
    div.search bar>
        input(type='text')
    
    div container.user>
        div conainter.notifacation bell
        img.user avatar
        span.user name{user name}
    div.main>
        img. avatar main
        p.greet{'Hi, there'}
        span. name main{User Name @ Handle}
    div.buttons>
        button.new+button.upload+button.share
```
```css
header{
    grid area 1/2/2/4;
    display grid 1fr 1fr/1fr 1fr;
}
search-bar{
    flex display
    center content
}
#search{
    width/height
}

usermain{
    grid
    grid template 1fr 1fr/auto 1fr
    gap
}

buttons{
    grid 3*1fr align/justify:center gap 10px
}
```

---

## Content
Content is divided further into three sections: Your Projects, Announcments, trending.

<b>Projects:</b> contains a series of cards laid out in a gird like pattern with a visible gap, where brief 
descriptions of the project is displayed. This occupies 2/3 of the content box and is positioned to the left

<b>Announcements:</b> is a column list of cards, not separated by any gap, where each card details a brief 
summary of the events. This cell occupies the last 1/3 of the top of the content box, and 1/2 of the y-axis.

<b>Trending:</b> Occupies the last 1/3 of the bottom content box as well, and takes up the second half of the y-axis
in conent. It is another series of cards with no gap, comprised of user handles, their avatars, and the title of their
trending project.

### Psuedo Code

```html
div.content>
    div.projects{Projects}>
        div.cards#projects*6>div.color bar+div.project-info>h3+p^img*3
    div.an-trend>
        div.announcements{announcments}>
            div.cards#announcments*3>h5+p 
        div.trending{trending}>
            div.cards#trending*3>img+h5+p 
```

```css
content{
    grid-area 2/2/4/-1
    display grid | columns: 4fr 1fr
}
project{
    column 1/2
    display grid | column: repeat(2, minmax(100px, 1fr))
}
h2{
    column 1/-1
}
an-trend{
    column 2/3
    display grid | rows: repeat(2, 1fr)
}
announcments, trending{
    display flex | flex-direction: columns| justify-content: space-around
}
```

# Future endeavors
This project is being submited with no interactivity. Future goals with this page will be to include a light
dark theme; a property that gets user prefrence for that mode; JS that animates and changes button and icons
when clicked; and better shading in the search field.