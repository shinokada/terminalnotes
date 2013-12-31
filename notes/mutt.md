# Notes on Email Client Mutt

## Resources
- [mutt.org](http://www.mutt.org/)
- [Archlinux](https://wiki.archlinux.org/index.php/mutt)
- [Mutt doc](http://www.therandymon.com/woodnotes/mutt/using-mutt.html)
- [Mutt html doc](http://www.mutt.org/doc/manual/)
- [Mutt manual](http://www.mutt.org/doc/manual.txt)
- [Mutt Wiki](http://dev.mutt.org/trac/wiki/MuttWiki)
- [Mutt FAQ](http://dev.mutt.org/trac/wiki/MuttFaq)
- [Mutt blog](http://empt1e.blogspot.jp/2009/10/using-mutt-with-gmail-imap-complete.html)


## URL in emails
[Stackoverflow](http://superuser.com/questions/695140/how-to-jump-to-links-and-open-it-in-mutt)

Add the following to .muttrc.

    macro index,pager \cB ": unset wait_key; set pipe_decode\n|w3m\n: set wait_key; unset pipe_decode\n" "call w3m to extract URLs out of a message"

Add the following to .mailcap.

    text/html; w3m -I %{charset} -T text/html; copiousoutput;    
    # or
    text/html; w3m %s; nametemplate=%s.html


Go to an individual email by hitting `Enter`.

ctrl-b to change to w3m and hit `:` to highlight links. 

Use tab to jump to the next link.


