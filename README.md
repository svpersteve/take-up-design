# Take Up Design

We encourage young people to take up UX and design as a career and to learn how to use design thinking in everyday life through fun after school clubs in London secondary schools.

## About this app

This is the [Middleman](https://middlemanapp.com/) app we use to develop the [Take Up Design website](http://takeupdesign.com/). It's a static site generator that converts all the haml and sass into html and css and throws it into a 'build' folder, which is then deployed to a separate GitHub Pages repo which publishes its master branch on GitHub Pages.

There's a [Rake task to automate deployment](https://github.com/svpersteve/take-up-design/blob/master/Rakefile), which just rebuilds the site then force pushes it to the GitHub Pages repo. Run `rake publish` to re-build the site and push to production.
