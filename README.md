# jquery.modallink

## Basic usage   

    $(".modal-link").modalLink();            

## Open link with additional data

    $(".modal-link-with-data").modalLink({
        showTitle: false,
        data: {
            foo: "bar"
        }
    });

## Open link with additional data with POST

    $(".modal-link-posting-data").modalLink({
        method: "POST",
        showTitle: false,
        data: {
            foo: "bar"
        }
    });

## Open in script

    $(".btn-click-me").click(function () {
        $.modalLink.open("Page1.html", {
            title: "Title"
        });  
    });

## Open unbound link in modal

    $.modalLink("open", $link);

## Close modal window inside modal

    (function (w) {
        $(".close-modal").click(function () {
            w.$.modalLink("close");
        });
    })(window.parent);

## Close modal with callback

    $.modalLink("close", function() {});

## Methods

### open
TBD

### close
TBD

## Events

### modallink.close
TBD

## Options

### title

Sets modal window title.
It can be set through attribute **data-ml-title** or **title**. If not any of these attributes is set, value will be selected form link text.

        <a href="target-url" data-ml-title="Edit content">link</a>
        <a href="target-url" title="Edit content">link</a>
        <a href="target-url">Edit content</a>
        
or with options when initializin modal link

        $link.modalLink({
            title: "Edit content"
        });
        
Value is always fetched from options first. 

So the priority list of defined title values looks like this:
* options value
* data-ml-title attribute value
* title attribute value
* link text

**NOTE:** Title do not have default value.

### showTitle

Sets if modal window titlebar is shown.
Can be set through **data-ml-show-title** attribute.

        <a href="target-url" data-ml-show-title="false">link</a>
        
or via options

        $link.modalLink({
            showTitle: false
        });

If none of above is set, value will be fetched from defaults. [See defaults](README.md#Defaults).

Priority list of showTitle value looks like this:
* options
* attribute
* default

### showClose

Sets if close button is shown on modal window titlebar.
Can be set through **data-ml-show-close** attribute.

        <a href="target-url" data-ml-show-title="false">link</a>
        
or via options

        $link.modalLink({
            showClose: false
        });
        
If none of above is set, value will be fetched from defaults. [See defaults](README.md#Defaults).

Priority list of showClose value looks like this:
* options
* attribute
* default

### width 

Sets modal window content width.
It can be set through **data-ml-width** attribute

        <a href="target-url" data-ml-width="400">link</a>
        
or with options when initializin modal link

        $link.modalLink({
            width: 400
        });
        
Value is always fetched from options first. 
If none of above is set, value will be fetched from defaults. [See defaults](README.md#Defaults).

So the priority list looks like this:
* option
* attribute
* default

### height

Sets modal window content height.
It can be set through **data-ml-height** attribute

        <a href="target-url" data-ml-height="400">link</a>
        
or with options when initializin modal link

        $link.modalLink({
            height: 400
        });
        
Value is always fetched from options first. 
If none of above is set, value will be fetched from defaults. [See defaults](README.md#Defaults)

So the priority list looks like this:
* option
* attribute
* default

### method

* REF
* CLONE
* GET
* POST

### data
### overlayOpacity
### $form

### disableScroll

### onHideScroll

hide scroll callback

##Styling

* .sparkling-modal-container
* .sparkling-modal-overlay
* .sparkling-modal-frame
* .sparkling-modal-title
* .sparkling-modal-title span
* .sparkling-modal-close
* .sparkling-modal-content

## Defaults

TBD

## Templates

TBD
