---
date: 2017-06-29T08:42:09+02:00
title: "hugo server"
slug: hugo_server
url: /commands/hugo_server/
---
## hugo server

A high performance webserver

### Synopsis


Hugo provides its own webserver which builds and serves the site.
While hugo server is high performance, it is a webserver with limited options.
Many run it in production, but the standard behavior is for people to use it
in development and use a more full featured server such as Nginx or Caddy.

'hugo server' will avoid writing the rendered and served content to disk,
preferring to store it in memory.

By default hugo will also watch your files for any changes you make and
automatically rebuild the site. It will then live reload any open browser pages
and push the latest content to them. As most Hugo sites are built in a fraction
of a second, you will be able to save and see your changes nearly instantly.

```
hugo server [flags]
```

### Options

```
      --appendPort                 append port to baseURL (default true)
  -b, --baseURL string             hostname (and path) to the root, e.g. http://spf13.com/
      --bind string                interface to which the server will bind (default "127.0.0.1")
  -D, --buildDrafts                include content marked as draft
  -E, --buildExpired               include expired content
  -F, --buildFuture                include content with publishdate in the future
      --cacheDir string            filesystem path to cache directory. Defaults: $TMPDIR/hugo_cache/
      --canonifyURLs               if true, all relative URLs will be canonicalized using baseURL
      --cleanDestinationDir        remove files from destination not found in static directories
  -c, --contentDir string          filesystem path to content directory
  -d, --destination string         filesystem path to write files to
      --disable404                 do not render 404 page
      --disableKinds stringSlice   disable different kind of pages (home, RSS etc.)
      --disableLiveReload          watch without enabling live browser reload on rebuild
      --disableRSS                 do not build RSS files
      --disableSitemap             do not build Sitemap file
      --enableGitInfo              add Git revision, date and author info to the pages
      --forceSyncStatic            copy all files when static is changed.
  -h, --help                       help for server
      --i18n-warnings              print missing translations
      --ignoreCache                ignores the cache directory
  -l, --layoutDir string           filesystem path to layout directory
      --meminterval string         interval to poll memory usage (requires --memstats), valid time units are "ns", "us" (or "??s"), "ms", "s", "m", "h". (default "100ms")
      --memstats string            log memory usage to this file
      --noChmod                    don't sync permission mode of files
      --noTimes                    don't sync modification time of files
      --pluralizeListTitles        pluralize titles in lists using inflect (default true)
  -p, --port int                   port on which the server will listen (default 1313)
      --preserveTaxonomyNames      preserve taxonomy names as written ("G??rard Depardieu" vs "gerard-depardieu")
      --renderToDisk               render to Destination path (default is render to memory & serve from there)
  -s, --source string              filesystem path to read files relative from
      --stepAnalysis               display memory and timing of different steps of the program
  -t, --theme string               theme to use (located in /themes/THEMENAME/)
      --themesDir string           filesystem path to themes directory
      --uglyURLs                   if true, use /filename.html instead of /filename/
  -w, --watch                      watch filesystem for changes and recreate as needed (default true)
```

### Options inherited from parent commands

```
      --config string    config file (default is path/config.yaml|json|toml)
      --log              enable Logging
      --logFile string   log File path (if set, logging enabled automatically)
      --quiet            build in quiet mode
  -v, --verbose          verbose output
      --verboseLog       verbose logging
```

### SEE ALSO
* [hugo](/commands/hugo/)	 - hugo builds your site

###### Auto generated by spf13/cobra on 29-Jun-2017
