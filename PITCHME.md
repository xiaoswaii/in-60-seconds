# 串接API做出PHOTO ALBUM

---

## 一開始....

```
$.ajax({
  url: 'https://emma.pixnet.cc/album/elements?set_id=34260&user=emmademo',
  type: 'GET',
  success: function(data) {
    var elements  = data.elements;
    for(var x = 0 ; x<elements.length ; x++){
      if(elements[x].type === 'pic'){
        var pic = elements[x].thumb;
        var link = elements[x].link;
        var title = elements[x].title;
        var node = "<li><a href='"+link+"'>"+"<img src='"+pic+"'></a><span>"+title+"</span></li>";
        $("ul").append(node);
      }
    }
  },
  error: function(e) {
	   console.log(e.message);
  }
});
```

![](assets/img/presentation.png)

---
@title[Customize Slide Layout]

@snap[west span-50]
## Customize Slide Content Layout
@snapend

@snap[east span-50]
![](assets/img/presentation.png)
@snapend

---?color=#E58537
@title[Add A Little Imagination]

@snap[north-west]
#### Add a splash of @color[cyan](**color**) and you are ready to start presenting...
@snapend

@snap[west span-55]
@ul[spaced text-white]
- You will be amazed
- What you can achieve
- *With a little imagination...*
- And **GitPitch Markdown**
@ulend
@snapend

@snap[east span-45]
@img[shadow](assets/img/conference.png)
@snapend

---?image=assets/img/presenter.jpg

@snap[north span-100 headline]
## Now It's Your Turn
@snapend

@snap[south span-100 text-06]
[Click here to jump straight into the interactive feature guides in the GitPitch Docs @fa[external-link]](https://gitpitch.com/docs/getting-started/tutorial/)
@snapend
