### the mind of ra the wolf
a digital form of of my philosophies: my mind. It started as a blog which was a sorta philosophical diary intended for the public, that i started when i was 15

i have philosopher personality, and sometimes i express myself through writing, creating a life-llng philosophical diary.

i have my own unique thoughts, ideas, concepts. Those concepts build up to make my own language, or at least patterns ( a 'pattern language'?) Anyway, it's worth keeping my own view of the world in tact.
- - -

### notes

#### import from wordpress
ho. ly. shit. that one bad decision of using wordpress instead of writing my own site generator costed me. :(

currently:
the current `_posts` are from the python script
the current `_drafts_ are from the python script
  - TODO: only 5 drafts were exported, need to merge with the other two imports (about 80?)
the current `_pages` folder were imported from the wordpress plugin (with toc), then edited, so merge carefully
  - TODO: merge all pages
    - merged the headers of the miscellenous pages: blog 'n archives
    - merged the herro.md
    - only portfolio and valuable things written are left
  - resume is copy paste, so no worries there
  - portfolio has some new junk on the top, but that's about it
  - herro was preserved as is
  - archives was sorta merged, no worries though


- see diff.txt file in root to see differences between the different importers
  - still need to try import via database (should be easy!)
  - this importer tool looks easy too!: https://github.com/some-programs/exitwp
    - one of the above should be perfect...?
  - https://import.jekyllrb.com/docs/wordpressdotcom/ has a link to a good tutorial with lots of code snippets too

  - **for now, use the xml one because it preserves endlines with breakline tag, then i need to find a way to remove the 'blog' from the permalink key in the front matter, and that would be good enough!**, then, though not needed, can replace the breakline html tag with two spaces (for markdown breakline)
    - a simple script that checks the front matter for 'permalink' key, then remove the blog part
    - https://unix.stackexchange.com/questions/432499/find-a-pattern-and-replace-its-value-in-shell-script
    - just use sed, figure out regular expressions, replace, git push, check changes of the commit
- check this commit for when i replaced the exported files [remove toc](https://github.com/rahil627/mind-of-rathewolf/commit/dd4f9e13cba174a94e385ee18b71bb5bb83cf886)
- currently: the posts and drafts come from jekyll export dated 11-01-2022, but, i don't think it exported pages...? re-check this. i think the current pages come from the older jekyll export (2020?)
  - eh, i trashed that older jekyll import... oops?
- it's starts by porting my old blog (Wordpress!!! lolll... yiikes!!




- this is one repo that should have an appropriate license...
- add The Mind of Ra crowd-funding writings
- re-directs: mindof, themindof, blog, philosophy, philo
- make this repo private, but be warned: you cannot use GitHub Pages on a private repo

temp:
should use Wordpress to backup to an xml file first

https://import.jekyllrb.com/docs/wordpress/
  - official importers
  - https://github.com/jekyll/jekyll-import

https://talk.hyvor.com/blog/migrate-from-wordpress-to-jekyll/
  - uses an outdated plugin, but not bad
