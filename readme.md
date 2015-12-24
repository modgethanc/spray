spray
=====

a long time ago, i wrote this nasty pile of perl bullshit to make myself a custom static bloglike thing. this is the result. i did not make it with the intention that it would be easy for someone else to pick up and use, but i wanted to make it easy for me to remember how it works, so i'm dumping some documentation here.

if you use it and want to show me what you're doing, i would be happy to see it!

to use
------

under 'content', you put text files. use the following filename formats:
  * `texts.{*name*}.txt` will make a standard spraypost
  * `drafts.{*name*}.txt` will make a post that does not appear in the main post list, but will render fully so you can sanity-check it. all drafts are linked from drafts.html
  * `backlog.{*name*}.txt' is a special type of spraypost that doesn't appear in the main post list, but can be read like any other post, and is listed under backlog.html
  * `meta.{*name*}.txt` will make a metapage that doesn't get treated like a normal post, but you can link to it as reference

the script will pull whatever you use for {*name*} and make that the filename. for example, `texts.happy.txt` will render to `happy.html`. for this reason, it is super duper important that you never reuse names between posts. for example, if you have `texts.happy.txt` and `backlog.happy.txt`, one of them will clobber the other. the script is merciless. it does not care what you intended. sorry.

post formatting
---------------

the first line will be taken as the title of the post, which includes what title is displayed in post listing. the last line is parsed out for #tags like all the cool blogs have. inline html works as normal.

config
------

you can configure things like how many posts to show where, what you're using for templates, change the default directory structure, other bullshit. this is probably easy to break, because nothing in this script is robust.
