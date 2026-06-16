# Note templates (aka note duplication)

> [← Help Index](../00-index.md) · Category: [Notes & Writing](./index.md) · [Source ↗](https://www.amplenote.com/help/using_note_templates)

## Intro

**Template** = a note that can be reused multiple times (eg. checklists, meeting notes, repetitive processes etc.)

**Template** (in Amplenote) = a note that is locked and titled with "Template:" at the beginning

**Note UUID** = the internal identifier of a note inside your notebook; inside the URL of a note, the UUID lies after `amplenote.com/notes` and before any `?` sign

**Public note token** = the external (public) identifier of a published note

Note templates in Amplenote enable you to quickly create repetitive scenarios and duplicate the content of other notes. You can also share your templates with the web by using "new note links."

💡 **Also check out:** this annual review template

## Inserting a template into an existing note

Given an existing template in your notebook (eg. a "daily startup" template you might want to insert into your jot every day, you can simply use:

`@=`

an "at" sign followed by an "equal" sign to start searching for the name of your template.

`@=` and `[[=` are equivalent

`@=` is just one of many ways to use note linking capabilities in Amplenote. Check out: Note linking guide (at @ and double-bracket `[[` notation)#Inserting a section of another note.

## Creating a new note from a template

As an alternative, you can also create a note from a certain template note. Given an existing note that serves as your template:

1. Preface the template note title with `Template:`
2. Lock the template note

Now, when you type the name of the template in Quick Open (which you can access with `Ctrl-O` or `Cmd-O`), you will see an option to create a new note based on your template.

_When a note starts with the word "Template:" and has been locked (Triple dot -> More Options -> Lock Note), you'll be given an option from the Quick Open menu to create a copy of it_

Clicking on that second option will open a new note where you can change the title to include today's date.

💡 **Optional suggestion**: Apply a tag like `templates` to all of your templates, to keep them nicely organized and easy to find.

## Creating a gallery of templates using the "new note" link

You can create links that will beget the creation of notes from existing templates. To do so, you start by defining a link that will create a new note: `https://www.amplenote.com/notes/new`. Then you can add any of the optional parameters to customize your new note:

- the `source` parameter is used to specify the note **UUID of the template that is to be duplicated**
- the `name` parameter specifies **the initial name for the new template instance**
- the `tags` parameter accepts **a list of comma separated tags to add to the newly created note**

For example, if you have a template called "Template: Bonanza Manager review for Employee" with the note UUID `ABC123`, the following link will duplicate that template while renaming it "Bonanza Employee review" and adding the tags "bonanza/reports" and "shared".

```
https://www.amplenote.com/notes/new?source=ABC123&name=Bonanza%20Employee%20Review%3A%20&tags=bonanza/reports,shared
```

Notice how links that will create a new note use a different Rich Footnote icon than a vanilla link would use.

## Sharing note templates

Remember the "new note link" functionality? Well, it works with public notes too. If you want to share a template with the Internet, all you have to do is:

1. Publish your template note using the note options
2. Create a new note link, and set the `source` parameter to `public-1234`, where `1234` is your public note token
3. Share your new note link with the world!

Say my public note URL is `/help/using_note_templates`. That means my public note token is `cypvuTF7d1LCXNy5CDGYhM9H`. So my template URL will be

```
https://www.amplenote.com/notes/new?source=public-cypvuTF7d1LCXNy5CDGYhM9H
```

When someone clicks on my link, they will see a new Amplenote window being open (prompting them to login or create an account if one is not found in their browser). After the user is logged in, the source note I created will be duplicated into that user's notebook.

Note that public new note links work with the same parameters, so "title" and "tags" are supported here as well!
