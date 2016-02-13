### 1.7 Генерация URL {#1-7-url}

*   в контроллере

```$url = $this->generateUrl( 'blog_show', array('slug'=>'my-bkig-post') );```

*   в js файлах

```var url = Routing.generate( 'blog_show',{"slug":'my-blog-post'} );```

*   в шаблонах TWIG

```<a href="{{ path( 'blog_show',{'slug':'my-blog-post'} ) }}">Read post</a>```