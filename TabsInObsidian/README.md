# Mostly-CSS Tabs in Obsidian
---
⚠ Live Preview users,  please see [below](#live-preview)! ⚠

This is an implementation for a tab-based rendering scheme in Obsidian.md, leaning heavily on capabilities offered by the native callouts feature of the app. The snippet is available in this repository or at [this link](TabsInObsidian.css). We use mostly CSS and a very minor amount of inline HTML to get everything working properly. To get started, you'll want to be familiar with the [basic syntax of callouts](https://help.obsidian.md/How+to/Use+callouts).  

## The Callouts
We will be using two types of callout to help us with structure, and a third type to hold our desired content:
- `[!tabbed-box]` is the outermost callout and will serve as a container for any tabs and content that you want to have grouped together.
- `[!tabs]` is the mid-level callout, and will hold all of the content that you want to divide between your various tabs. This one is required for formatting purposes.
- `[!tab-content]` is a reusable innermost callout that holds the actual markdown content that you want to see in each tab.

The basic structure inside the actual note will look something like this:
```md
> [!tabbed-box]
> %% input declarations go here %%
> %% label declarations go here %%
>
> > [!tabs]
> > > [!tab-content]
> > > This is stuff in the first tab.
> >
> > > [!tab-content]
> > > These are things in the second tab!
> > > The second tab is cozy.  
```

Overall, there's nothing too complex here from a callouts perspective, just a lot of nesting which can be somewhat uncomfortable sometimes.

## The HTML
However, we *do* have an important step that we still need to take care of, and that's our inputs and labels to make the whole thing tick. All of our CSS is based on hiding radio buttons and prettying-up some HTML label tags that we can refer to with our CSS selectors. Let's see what a declaration for a single input and label would look like:
```md
> <input type="radio" id="first1" name="tab-group-1" checked>
> <label for="first1">The First Label Title!</label>
```
Without getting too deep into the HTML explanation of what all this means, there are a few bits to be cognizant of:
- `id="first1"` is an example of a radio button's internal ID and is required to be unique within any single note. For syntax reasons, each ID within a given group must end with the number of its index, such as 1, 2, 3, etc. More examples of valid IDs would be `id="MyTab1"` for a first tab's label, `id="portrait-2"` for a second tab's label, and so on. The crucial feature here is that the ID ends with the number that corresponds to its place in the order of the group.
- `name="tab-group-1"` is the name of the group to which an input belongs. These can be named anything you like, as long as all inputs within the same group have the same name, and each group's name is different.
- `for="first1"` is a property that connects our styled label to the underlying radio button input. Notice that our `for` value here is the same as our example `id` above. These must be the same in order to bind the label to the input.
- `The First Label Title!` is the actual text content that will render inside the tab label, and can be whatever you want.

And that's really all that we need on the HTML side. If you want a full demo to read through, check out [example.md](example.md).

---
## Live Preview
As of Obsidian v0.14.6, this snippet will not fully work in Live Preview. It will partially work in editing view, and will only work in reading view if the pane in which a given note is opened in has not yet been in editing view *at all*. This means that in order to have any reasonable functionality of the snippet in Live Preview, you must also have your default new pane view be reading mode. If this requirement is not met, then the labels rendered in reading mode will not correctly bind to their hidden radio button inputs, preventing you from changing tabs.

Additionally, Live Preview's parsing of note markdown can interfere with correct operation of the snippet even with the above prerequisites satisfied. In order to guarantee that a given tab group will function, you must essentially sanitize the preceding indents. Here is an example:
```md
> >

> [!tabbed-box]
> etc.
```

If you don't want to have to see those extra indents and such in reading view, you can comment them out like so:
```md
%%> >%%

> [!tabbed-box]
> etc.
```

Congratulations! Now you should have at least a little bit of proper functionality in Live Preview.
