# The blog
This is the source code of DNF's blog. You can visit it on
[https://rpm-software-management.github.io](http://rpm-software-management.github.io).

# How to write a new article
1. Write the article
2. Create a new file in the `/_post` directory that follows the convention `YYYY-MM-DD-name-of-post.html` or `YYYY-MM-DD-name-of-post.markdown`
3. The file consists of two part devided by `---`

    ```
    ---
    layout: post
    title:  "Title of your post"
    date:   2017-10-24 12:28:44 +0100
    author: your_name <email@address>
    visible: 1
    categories: devided by space
    ---
    Here put your article in html or markdown
    ```

Don't forget to change the title, date, author and categories

5. Put your article into that file and style it properly
5. Test how your article will really look like.
6. Create commit and push to the master

#Testing
When writing code it is normal to make errors. And since creating a new blog is
*"writing code"* you can make some as well. Therefore before pushing yours article
you should check three thinks:

1. Article does not include grammatical and typing errors
2. Article will be displayed
  * ...as a newest article
  * ...with correct title and date
3. Article is styled correctly

Testing of second two can be tricky, but thankfully there is a easy way of doing so.
First, you will need to install some Ruby gems. Please run:

    # dnf install rubygem-jekyll ruby-devel
    $ bundle install

Then you should be ready to run:

    $ bundle exec jekyll serve

This will locally deploy the whole website. Click a link provided by this command
(probably will be [http://localhost:4000](http://localhost:4000))

Now you can see the front page. Make sure your article is on the top, click it and
check it.

When you make change, there is no need to restart the local server - just let
it run and when file is edited, it will be automatically uploaded. You need to only
refresh the site in your browser.

## Credits
[Original theme](https://startbootstrap.com/template-overviews/clean-blog/) - modified a bit
