---
views:
    flash:
        region: flash
        template: anax/v2/image/default
        data:
            src: "image/theme/bg.jpg?width=1100&height=150&crop-to-fit&area=0,0,30,0"
    main:
        template: anax/v2/article/default
        data:
            class: blog

    byline: false
    block-about: false
    article-toc: false

    blog-list:
        region: main
        template: anax/v2/blog-list/default
        sort: 2
        data:
            dateFormat: j F Y
            meta: 
                type: toc
                orderby: publishTime
                orderorder: desc

    blog-toc:
        region: sidebar-right
        template: anax/v2/blog-toc/default
        sort: 2
        data:
            meta: 
                type: copy
                view: blog-list

---
Dagens Bild
===========================

Detta är en kort liten blogg om några fina bilder.
