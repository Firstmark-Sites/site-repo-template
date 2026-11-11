# {{DOMAIN}}

Site code under git (Firstmark Site Care). The live site is backed up every night and mirrored;
changes reach the site only through a reviewed deploy, never by editing files on the server.

- `wp-content/themes`, `wp-content/mu-plugins`, non-core files in the docroot (`.htaccess`, `.user.ini`…).
- `plugins.lock` — third-party plugins with versions (their code is not stored).
- Not here: WordPress core (checked nightly against wordpress.org), `wp-config.php`, uploads, caches.

Every night the mirror of the live site is compared with `main`: a file changed, added or removed
outside git (FTP, the theme editor, a hack) raises an alert for the team that maintains the site.
After an intended change made on the live site, commit it here so the next check is clean.
