Boostrap Alert Popover
============
## and a `focus` trigger fix

Extension to usual [bootstrap's popovers](http://getbootstrap.com/javascript/#popovers), adding a new `mode` and `trigger` option to display
an alert close button.

Also added a new trigger called `click-outside`. This is supposed to fix the `focus` trigger behavior. The popover is not 
dismissed when the popover itself is clicked, opposed to the default `focus` trigger. The `click` trigger is still used to show 
the popover.

Test it at [JSFiddle](http://jsfiddle.net/tB9s3/).

**NOTE:** this was built from http://getbootstrap.com/customize/?id=362b4aade57c034ccfdc
 / https://gist.github.com/362b4aade57c034ccfdc . Which only includes Bootstrap's tooltip, popover and alert.
 
 This overrides the following CSS rules:
 

```
.popover-title {
//  original: 8px 14px; 
    padding: 2px 0px;
//  original: normal;
    font-weight: bold;
}

.popover-content {
//  original: 9px 14px;
    padding: 9px 5px;
}

.popover {
//  original: 1px;
    padding: 8px 14px;
}
```

## Usage ##
-----------

#### Inline ####

Use the `data-mode` attribute in your HTML

```
<button type="button" id="my-button" data-mode="alert" title="My title" data-content="This is the popover content.">Show alert popover</button>
```

#### Javascript ####

Pass `mode: 'alert'` in the `jQuery` constructor

```
$("#my-button")
    .popover({ 
        trigger: 'click', 
        title: 'My Title', 
        content: 'This is the popover content.', 
        mode: 'alert' 
    });
```

**Use the `click-outside` trigger if you want the popover to be dismissed when user clicks outside of it.** (`focus` dismisses
the popover even if you click on it)