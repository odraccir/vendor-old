GitHub Flavored Markdown
================================
GitHub uses what we're calling "GitHub Flavored Markdown" (GFM) for messages, issues, and comments. It differs from standard Markdown (SM) in a few significant ways and adds some additional functionality.

If you're not already familiar with Markdown, you should spend 15 minutes and go over the excellent [Markdown Syntax Guide](http://daringfireball.net/projects/markdown/syntax) at Daring Fireball.

# Differences from traditional Markdown

## New Lines
The biggest difference that GFM introduces is in the handling of linebreaks. With SM you can hard wrap paragraphs of text and they will be combined into a single paragraph. We find this to be the cause of a huge number of unintentional formatting errors. GFM treats newlines in paragraph-like content as real line breaks, which is probably what you intended.

The next paragraph contains two phrases separated by a single newline character:

> Roses are red
> Violets are blue

becomes

Roses are red
Violets are blue

## Multiple underscores in words
It is not reasonable to italicize just part of a word, especially when you're dealing with code and names often appear with multiple underscores. Therefore, GFM ignores multiple underscores in words.

> perform_complicated_task
> do_this_and_do_that_and_another_thing

becomes

perform_complicated_task
do_this_and_do_that_and_another_thing

## URL autolinking
GFM will autolink standard URLs, so if you want to link to a URL (instead of setting link text), you can simply enter the URL and it will be turned into a link to that URL.

## Fenced code blocks

Markdown converts text with four spaces at the front of each line to code blocks. GFM supports that, but we also support fenced blocks. Just wrap your code blocks in ``` and you won't need to indent manually to trigger a code block.

If you are indenting your code blocks with spaces, keep in mind that code within lists needs to be indented eight times in order to be properly marked as a code block.


## Syntax highlighting
We take code blocks a step further and add syntax highlighting if you request it. In your fenced block, add an optional language identifier and we'll run it through syntax highlighting. For example, to syntax highlight Ruby code:

> ```ruby
> require 'redcarpet'
> markdown = Redcarpet.new("Hello World!")
> puts markdown.to_html
> ```

We use [Linguist](https://github.com/github/linguist) to perform language detection and syntax highlighting.

## Task Lists

Further, lists can be turned into Task Lists by prefacing list items with [ ] or [x] (incomplete or complete, respectively).

> - [x] @mentions, #refs, [links](), **formatting**, and <del>tags</del> supported
> - [x] list syntax required (any unordered or ordered list supported)
> - [x] this is a complete item
> - [ ] this is an incomplete item

This feature is enabled for Issue and Pull Request descriptions and comments only. In those contexts, task lists will be rendered with checkboxes that you can check on and off.

See the [Task Lists blog post](https://github.com/blog/1375-task-lists-in-gfm-issues-pulls-comments) for more details.

## Quick quoting
Typing r on your keyboard lets you reply to the current issue or pull request with a comment. Any text you select within the discussion thread before pressing r will be added to your comment automatically and formatted as a blockquote.

## Name and Team @mentions autocomplete

Typing an @ symbol will bring up a list of people or teams on a project. The list will filter as you type, so once you find the name of the person or team you are looking for, you can use the arrow keys to select it and then hit enter or tab to complete the name. For teams, just enter the @organization/team-name and all members of that team will get subscribed to the issue.

The result set is restricted to repository collaborators and any other participants on the thread, so it's not a full global search. It uses the same fuzzy filter as the file finder and works for both usernames and full names.

Check out the blog posts for more information about @mention autocompletes for [users](https://github.com/blog/1004-mention-autocompletion) and [teams](https://github.com/blog/1121-introducing-team-mentions).

## Emoji autocomplete
Typing : will bring up a list of emoji suggestions. The list will filter as you type, so once you find the emoji you're looking for, just hit tab or enter to complete the highlighted result.

## Issue autocompletion
Typing # will bring up a list of Issue and Pull Request suggestions. Type a number or any text to filter the list, then hit tab or enter to complete the highlighted result.

## Zen Mode (fullscreen) writing
Zen Mode allows you to go fullscreen with your writing. You'll find the Zen Mode button on comment, issue, and pull request forms across the site. 

## References

Certain references are auto-linked:

> * SHA: 16c999e8c71134401a78d4d46435517b2271d6ac
> * User@SHA ref: mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
> * User/Project@SHA: mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac
> * #Num: #1
> * User/#Num: mojombo#1
> * User/Project#Num: mojombo/github-flavored-markdown#1

becomes

* SHA: 16c999e8c71134401a78d4d46435517b2271d6ac
* User@SHA ref: mojombo@16c999e8c71134401a78d4d46435517b2271d6ac
* User/Project@SHA: mojombo/github-flavored-markdown@16c999e8c71134401a78d4d46435517b2271d6ac
* #Num: #1
* User/#Num: mojombo#1
* User/Project#Num: mojombo/github-flavored-markdown#1

