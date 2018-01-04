# Aria

###### Sources
- [mozilla](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA)
- [ARIA intro by Gez Lemon](http://dev.opera.com/articles/view/introduction-to-wai-aria/)
- [ARIA Best Practices](https://www.w3.org/WAI/PF/aria-practices/Overview.html)
- [Using ARIA](https://w3c.github.io/using-aria/)
- [HTML 5.1 Spec](https://www.w3.org/TR/html51/)

## Definition

WAI-Aria: Web Accessibility Initiative - Accessible Rich Internet Applications


#### Purpose

Defines ways to make web applications more accessible to people with disabilities.  This is especially helpful for apps with Ajax and Javascript.   

ARIA attributes are designed to be interpreted automatically by the browser and translated to the operating system's native accessibility API's.

## Notes

The ARIA specification is split up into three different types of attributes: [roles](#roles), [states](#states), and [properties](#properties).

### Guide-lines
1. If you can use a native HTML element [HTML51] or attribute with the semantics and behavior you require already built in, instead of re-purposing an element and adding an ARIA role, state or property to make it accessible, then do so.
2. Do not change native semantics, unless you really have to.
3. All interactive ARIA controls must be usable with the keyboard.
4. Do not use role="presentation" or aria-hidden="true" on a visible focusable element.
5. All interactive elements must have an accessible name.

### Roles

> Roles describe widgets that aren't otherwise available in HTML 4, such as sliders, menu bars, tabs, and dialogs

### States

> States describe the current interaction state of an element, informing the assistive technology if it is busy, disabled, selected, or hidden.

> The terms "states" and "properties" refer to similar features. Both provide specific information about an object, and both form part of the definition of the nature of roles. In this document, states and properties are both treated as aria-prefixed markup attributes. However, they are maintained conceptually distinct to clarify subtle differences in their meaning. One major difference is that the values of properties (such as aria-labelledby) are often less likely to change throughout the application life-cycle than the values of states (such as aria-checked) which may change frequently due to user interaction.

[Fantastic example of state changes via js and css the utilize states `aria-hidden` and serval ARIA properties](http://www.oaa-accessibility.org/example/39/)

It can be helpful to think of aria state attributes as ways to communicate presentational changes (done by CSS/JS) to screen readers.
Some examples may include:
- Adding borders to indicate form validity or focus
- Changing the color of a check-box
- Hiding/Showing content

Subset of ARIA states:
- aria-busy 
- aria-checked: indicates the state of a checkbox or radio button
- aria-current 
- aria-disabled: indicates that an element is visible, but otherwise inoperable
- aria-grabbed: indicates the grabbed state of an object in a drag-and-drop operation
- aria-hidden 
- aria-invalid 

Widget ARIA state attributes:
- aria-autocomplete
- aria-checked
- aria-disabled
- aria-errormessage
- aria-expanded
- aria-haspopup
- aria-hidden
- aria-invalid
- aria-label
- aria-level
- aria-modal
- aria-multiline
- aria-multiselectable
- aria-orientation
- aria-placeholder
- aria-pressed
- aria-readonly (property)
- aria-required
- aria-selected
- aria-sort
- aria-valuemax (property)
- aria-valuemin (property)
- aria-valuenow (property)
- aria-valuetext (property)

Live Region State Attributes
- aria-atomic (property)
- aria-busy
- aria-live
    has enumerated values:
    - "off" 
    - "polite": when reader is in an idle state, the content changes of this element will be announced
    - "assertive": when text content is updated the region is spoken immediately
    
- aria-relevant

Drag-and-Drop Attributes§

- aria-dropeffect (property)
- aria-grabbed

Relationship Attributes
- aria-activedescendant
- aria-colcount
- aria-colindex
- aria-colspan
- aria-controls
- aria-describedby
- aria-details
- aria-errormessage
- aria-flowto
- aria-labelledby
- aria-owns
- aria-posinset
- aria-rowcount
- aria-rowindex
- aria-rowspan
- aria-setsize


### Properties

> Properties describe characteristics of these widgets, such as if they are draggable, have a required element, or have a popup associated with them

Subset of ARIA properties:
- aria-atomic
- aria-controls
- aria-describedby
- aria-details
- aria-dropeffect
- aria-errormessage
- aria-flowto
- aria-haspopup
- aria-keyshortcuts
- aria-label
- aria-labelledby
- aria-live
- aria-owns
- aria-relevant
- aria-roledescription
