# wfmucast

WFMU, my favourite radio station, has a fantastic rolling archive (http://www.wfmu.org/table).

I wanted to be able to use iTunes to automatically download recent archives of
my favourite shows for offline listening (this will also work with other
podcatchers). I realized that they publish RSS feeds for the archives; and
thus, the XML from their RSS feeds could be transformed into the XML for a
podcast using a simple web app (HTML::Mason was my then-favourite web app
development tool).

**Here's how it works:**

* Run this code somewhere; e.g. http://example.com/wfmucast
* Choose a show to receive regularly as a podcast from http://www.wfmu.org/table; for example, This Is The Modern World.
* Note the two-letter code used for the show--you can see it by clicking through to the playlist archive for the show; in our example, for This Is The Modern World, the code is LM (http://www.wfmu.org/playlists/LM).
* In your podcatcher, enter the podcast URL as http://example.com/wfmucast?LM
* Behind the scenes, wfmucast will go and fetch the latest RSS for the show you've chosen and translate it into XML for an iTunes podcast.
* You should now be subscribed to This Is The Modern World, receiving new episodes when they are archived.

**Notes**

This assumes you know how to set up HTML::Mason ("an elegant weapon, for a more
civilised age"). If you don't, Google, CPAN, or
https://masonbook.houseabsolute.com/book/ will get you started.

**Next Steps**

Redo the whole thing in something more respectably modern (Node.js?), with proper tests.
