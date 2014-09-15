---
layout: page
title: How It Was
description: Video, photos and session materials
permalink: /how-it-was/
order: 2
identifier: how-it-was

gallery:
    photos:
        -
          img: https://c4.staticflickr.com/4/3846/14831165014_b1b35e60cb_c.jpg
          thumb: https://c4.staticflickr.com/4/3846/14831165014_b1b35e60cb_n.jpg
          alt:
        -
          img: https://c4.staticflickr.com/4/3894/14646911168_2b96e5721c_c.jpg
          thumb: https://c4.staticflickr.com/4/3894/14646911168_2b96e5721c_n.jpg
          alt:
        -
          img: https://c4.staticflickr.com/4/3923/14646984708_ced32044e6_c.jpg
          thumb: https://c4.staticflickr.com/4/3923/14646984708_ced32044e6_n.jpg
          alt:
        -
          img: https://c4.staticflickr.com/4/3878/14810638246_129fe6b97b_c.jpg
          thumb: https://c4.staticflickr.com/4/3878/14810638246_129fe6b97b_n.jpg
          alt:
        -
          img: https://c4.staticflickr.com/4/3882/14833302622_af12e7584e_c.jpg
          thumb: https://c4.staticflickr.com/4/3882/14833302622_af12e7584e_n.jpg
          alt:
        -
          img: https://c3.staticflickr.com/3/2928/14853573753_026bfc2a74_c.jpg
          thumb: https://c3.staticflickr.com/3/2928/14853573753_026bfc2a74_n.jpg
          alt:
        -
          img: https://c4.staticflickr.com/4/3879/14647186437_fa802dc498_c.jpg
          thumb: https://c4.staticflickr.com/4/3879/14647186437_fa802dc498_n.jpg
          alt:


---

<!-- -
          img: https://c4.staticflickr.com/4/3847/14527275067_dfc1c0a927_z.jpg
          thumb: https://c4.staticflickr.com/4/3847/14527275067_dfc1c0a927_n.jpg
          alt:
        -
          img: https://c2.staticflickr.com/6/5586/14733484523_bf2e858805_z.jpg
          thumb: https://c2.staticflickr.com/6/5586/14733484523_bf2e858805_n.jpg
          alt: -->
<div class="summary">We certainly had a great time at OKFestival and there was no shortage of cameras and computers to capture the fun (and the knowledge!). Get a closer look at what OKFestival 2014 was like in Berlin.</div>

## Video

Check out the official OKFestival YouTube playlist below, from <a title="Open Knowledge YouTube Channel" href="https://www.youtube.com/user/openknowledgefdn/">Open Knowledge</a>, and browse <a href="https://www.youtube.com/results?search_query=%23okfest14">community generated videos on YouTube #okfest14</a>.

<iframe src="//www.youtube.com/embed/videoseries?list=PLOGV29UsPM6icd01P6fwU74PQEAXL0H4q" height="315" width="560" allowfullscreen="" frameborder="0"></iframe>


## Pictures

A sampling of the images from the <a href="https://www.flickr.com/groups/okfestival2014/">OKFestival 2014 Flickr group</a>. Don't forget to add your pictures to the pool!

<div id="gallery-1">
<ul>
    <li class="grid-sizer"></li>
    {% for photo in page.gallery.photos %}
    <li><a href="{{photo.img}}" data-imagelightbox="e"><img src="{{photo.thumb}}" alt="{{photo.alt}}" /></a></li>
    {% endfor %}
</ul>
</div>

<script src="https://code.jquery.com/jquery-1.11.1.min.js"></script>
<!-- <script src="{{ "/static/js/vendor/masonry.pkgd.min.js" | prepend: site.baseurl }}" ></script>
 -->
<script src="/static/js/vendor/imagelightbox.min.js"></script>
<script>
    $( function()
    {
        // OVERLAY

            overlayOn = function()
            {
                $( '<div id="imagelightbox-overlay"></div>' ).appendTo( 'body' );
            },
            overlayOff = function()
            {
                $( '#imagelightbox-overlay' ).remove();
            },

         // ARROWS

            arrowsOn = function( instance, selector )
            {
                var $arrows = $( '<button type="button" class="imagelightbox-arrow imagelightbox-arrow-left"></button><button type="button" class="imagelightbox-arrow imagelightbox-arrow-right"></button>' );

                $arrows.appendTo( 'body' );

                $arrows.on( 'click touchend', function( e )
                {
                    e.preventDefault();

                    var $this   = $( this ),
                        $target = $( selector + '[href="' + $( '#imagelightbox' ).attr( 'src' ) + '"]' ),
                        index   = $target.index( selector );

                    if( $this.hasClass( 'imagelightbox-arrow-left' ) )
                    {
                        index = index - 1;
                        if( !$( selector ).eq( index ).length )
                            index = $( selector ).length;
                    }
                    else
                    {
                        index = index + 1;
                        if( !$( selector ).eq( index ).length )
                            index = 0;
                    }

                    instance.switchImageLightbox( index );
                    return false;
                });
            },
            arrowsOff = function()
            {
                $( '.imagelightbox-arrow' ).remove();
            };

            var instanceF = $( 'li a' ).imageLightbox(
        {
            onStart:        function() { overlayOn(); arrowsOn( instanceF, $( 'li a' ) ); },
            onEnd:          function() { overlayOff(); arrowsOff(); },
            onLoadStart:    function() {  },
            onLoadEnd:      function() {  $( '.imagelightbox-arrow' ).css( 'display', 'block' ); }
        });

    });




</script>

## Podcasts

<div class="pull">
    <figure>
    <a href="http://okcast.org/tag/okfestival2014/"><img alt="OkCast" src="http://2014.okfestival.org/wp-content/uploads/2014/09/OkCast_Logo_Horizontal_Color_Small-300x70.png" width="300" height="70" /></a>
    </figure>
</div>

<a href="https://twitter.com/alexfink">Alex Fink</a> brought the <a title="OKFestival podcasts at the OKCast" href="http://okcast.org/tag/okfestival2014/">OKCast</a> to OKFestival and produced extensive audio coverage of the event, including interviews with keynote speakers and other presenters.


<iframe width="100%" height="450" scrolling="no" frameborder="no" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/playlists/50785840&amp;auto_play=false&amp;hide_related=false&amp;show_comments=true&amp;show_user=true&amp;show_reposts=false&amp;visual=true"></iframe>


## Session notes

Detailed notes captured at the event, and in some cases amended after, are here on the session <a href="https://pad.okfn.org/p/Pad_of_Pads">Etherpads</a>. You can also <a title="Festival Programme" href="http://2014.okfestival.org/festival-programme/">browse the programme</a> to find a particular session, ones with notes have a button linking to the corresponding Etherpad.

If you are up for it, we could use some help <a href="http://wiki.okfn.org/OKFestival#OKFestival_Session_Notes_How_to">archiving the session notes on our wiki</a>.
