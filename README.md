### pyechonest
---
https://github.com/echonest/pyechonest

http://echonest.github.io/pyechonest/

```py
from pyechonest import config
config.ECHO_NEST_API_KEY="YOUR API KEY"

from pyechonest import artist
bk = artist.Artist('bikini kill')
print "Artists similar to: %s:" % (bk.name,)
for similar_artist in bk.similar: print "\t%s" % (similar_artist.name,)

from pyechonest import artist
weezer_results = artist.search(name='weezer')
weezer = weezer_results[0]
weezer_blogs = weezer.blogs
print 'Blogs about weezer:', [blog.get('url') for blog in weezer_blogs]

from pyechonest import artist
a = artist.Artist('lady gaga')
print a.id

from pyechonest artist
a = artist.Artist('musicbrainz:a74b1b7f-71a5-4011-9441-d0b5e4122711')
print a.name

from pyechonest import artist
for hottt_artist in artist.top_hott():
print hottt_artist.name, hottt_artist.hotttnesss

from pyechonest import song
rkp_results = song.search(artist='radiohead', title='karma police')
karma_police = rkp_results[0]
print karma_police.artist_location
print 'tempo:',karma_police.audio_summary['tempo'],'duration:',karma_police.audio_summary['duration']


from pyechonest import song
ss_results = song.search(artist='the national', title='slow show', buckets=['id:7digital-US', 'tracks'], limit=True)
slow_show = ss_results[0]
ss_tracks = slow_show.get_tracks('7digital-US')
print ss_tracks[0].get('preview_url')
```

```
```

```
```


