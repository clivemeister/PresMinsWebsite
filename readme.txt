git checkout -b new-post-feature
   - create a new branch in for the new page

hugo new content posts/my-post-name/index.md
   - creates the "./content/posts/my-post-name/index.md" as a starter for the new post, based on ./archetypes/default.md
   - NB, "./public" is for Hugo local test site, I think
   - it also uses /public up on the website, but that should be created by Render doing stuff before deployment
   - could do   hugo new content posts/my-new-post.md   for just a single file, rather than an index.md (leaf) node in directory called my-post-name
   - add my-image.jpg  to ./content/post/my-post-name/  if that's in the file


hugo server --buildDrafts
hugo server -D
   - to run local server that includes drafts

git add ./content/posts/*
   - stage changes

git commit -m "my new page is ready for testing"
   - all done for the moment and ready to review or push

git push origin new-post-feature
   - sends the new branch up to https://github.com/clivemeister/PresMinsWebsite

Go to repo on github.  
Click the "Compare & pull request" button.  
Select target (main) and candidate feature (new-post-feature)
Click "Create Pull request"

We could now review on Render, if we are using the "Pull request previews" feature.

When ready, on Github click "Merge pull request", using an appropriate method (squash and merge is probably appropriate here)

Switch to main and pull newest (merged) version:
 git checkout main
 git pull

Delete now-merged branch:
 git branch -d new-post-feature

Hosted on Render, via Github  (Render is clive@freeman.org.uk)
Ought to be automatically deployed, but seems to need you to log on to Render.com and poke it

## 2025-01-07
OK so now we should be set up with the following events:
 - {{Page Path}} for all pages
 - sign_up_started
 - sign_up_addpymt
 - login
 - new_goal_started
 - new_goal_finished
 - goal_deleted