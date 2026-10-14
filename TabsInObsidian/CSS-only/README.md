# Pure-CSS Tabs in Obsidian

Extremely rough version of CSS-only tabs, relying on fun new stuff.

## The Callouts

Two callout types are used for structure:

- `puretabs` is the containing callout for everything, similar to `tabbed-box` from the main snippet.
- `ptab` is used to designate each tab; callout metadata of each `ptab` IS RESERVED. The callout metadata is what becomes the virtual tab text, e.g. in the below example, the first tab's title / text / whatever is `Excla`.

### Example

```md
> [!puretabs]
> 
> > [!ptab|Excla]
> > 
> > It even works
> 
> > [!ptab|mation]
> > 
> > <span style="display:block;text-align:right;">while nested!?</span>
```
