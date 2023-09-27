# Mazda MX5


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
    <div id="album" class="grid" style="margin-top: 20px;">

    </div>
    <script src="https://cdn.jsdelivr.net/npm/jquery@3.7.1/dist/jquery.min.js"></script>
    <script src="https://unpkg.com/imagesloaded@5/imagesloaded.pkgd.min.js"></script>
    <script src="https://unpkg.com/masonry-layout@4/dist/masonry.pkgd.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/@fancyapps/ui@5.0/dist/fancybox/fancybox.umd.js"></script>
    <script type="text/javascript">

        var albums = [
            
            {
                url: '/mx5/images/1989.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/1990.jpg',
                desc: ''
            }, 
            {
                url: '/mx5/images/1991.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/1992.jpg',
                desc: ''
            }, 
            {
                url: '/mx5/images/1993.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/1994.jpg',
                desc: ''
            }, 
            {
                url: '/mx5/images/1995.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/1996.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/1997.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/1998.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/1999.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/1999.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/1999.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/2000.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/2001.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/2002.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/2003.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/2004.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/2005.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/2006.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/2007.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/2008.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/2009.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/2011.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/2012.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/2014.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/2015.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/2016.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/themenew.jpg',
                desc: ''
            },
            {
                url: '/mx5/images/1-2.jpg',
                desc: ''
            },
            
            
            {
                url: '/mx5/images/6.jpg',
                desc: ''
            }, 
            {
                url: '/mx5/images/1-1.jpg',
                desc: ''
            },
        ]

        var albumsStr = ''
        for (var i = 0; i < albums.length; i++) {
            albumsStr += ' <a class="grid-item" data-fancybox="gallery" data-src="' + albums[i].url + '" data-caption="234' + albums[i].desc + '"><img  src="' + albums[i].url + '"/></a>'
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

    </script>

</body>




</html>

---

> 作者: zebraoo  
> URL: https://zebraoo.blog/mx5/  

