Boostrap Alert Popover
=====================

Extension to usual [bootstrap popovers](http://getbootstrap.com/javascript/#popovers), adding a new `mode` option to display
an alert close button.

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
Use `data` attributes in your HTML

```
<button type="button" id="my-button" data-mode="alert" title="My title" data-content="This is the popover content.">Show alert popover</button>
```

#### Code ####
Pass `mode: alert` in the `jQuery` constructor

```
$("#my-button")
    .popover({ 
        trigger: 'click', 
        title: 'My Title', 
        content: 'This is the popover content.', 
        mode: 'alert' 
    });
```