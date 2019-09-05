clean bundle

> bundle clean --force

watch gem site changes

> jekyll serve --watch

run gem execu

> bundle exec jekyll serve

fix coding error
chcp 1252

gem uninstall eventmachine
gem install eventmachine --platform ruby

live watch
jekyll serve --livereload

hosting to github pages
git remote rm origin
git init
git checkout -b gh-pages
git add .
git commit -m "test init pages"
git remote rm origin
git remote add origin https://github.com/abodehq/blue-eye-docs.git
git remote -v
git push origin gh-pages

//made changes
git add.
git commit -m "msg"
git push origin gh-pages
