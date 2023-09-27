# 


<!DOCTYPE html
    PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">

<head>
    <meta charset="UTF-8" />
    <meta http-equiv="Content-Type" content="text/html; charset=gb2312">
    <title></title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fancyapps/ui@5.0/dist/fancybox/fancybox.css" />
    <style>
        .grid-item {
            width: 220px;
            margin-bottom: 3px;
            margin-left: 5px;
            margin-right: 5px;
        }
    </style>

</head>

<body>
    <div id="album" class="grid">

    </div>
    <script src="https://cdn.jsdelivr.net/npm/jquery@3.7.1/dist/jquery.min.js"></script>
    <script src="https://unpkg.com/imagesloaded@5/imagesloaded.pkgd.min.js"></script>
    <script src="https://unpkg.com/masonry-layout@4/dist/masonry.pkgd.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@fancyapps/ui@5.0/dist/fancybox/fancybox.umd.js"></script>
    <script type="text/javascript">

        var albums = [
            {
                url: '/album/images/avatar.jpg',
                desc: '头像'
            },
            {
                url: '/album/images/20230927.jpg',
                desc: '20230927雨后晚霞'
            },
        ]

        var albumsStr = ''
        for (var i = 0; i < albums.length; i++) {
            albumsStr += ' <a class="grid-item" data-fancybox="gallery" data-src="' + albums[i].url + '" data-caption="' + albums[i].desc + '"><img  src="' + albums[i].url + '"/></a>'
        }

        console.log('albumsStr---> ', albumsStr)

        document.getElementById('album').innerHTML = albumsStr


        Fancybox.bind('[data-fancybox="gallery"]', {
            
        });

        var $grid = $('.grid').masonry({
            // options...
        });
        // layout Masonry after each image loads
        $grid.imagesLoaded().progress(function () {
            $grid.masonry('layout');
        });


        // https://masonry.desandro.com/layout
        // https://imagesloaded.desandro.com/
        // https://fancyapps.com/fancybox/getting-started/
        // https://jsfiddle.net/tgcpey0m/

    </script>

</body>




</html>

---

> 作者: zebraoo  
> URL: https://zebraoo.blog/album/  

