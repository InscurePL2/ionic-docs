---
title: "ion-segment"
---
import Props from '@ionic-internal/component-api/v8/segment/props.md';
import Events from '@ionic-internal/component-api/v8/segment/events.md';
import Methods from '@ionic-internal/component-api/v8/segment/methods.md';
import Parts from '@ionic-internal/component-api/v8/segment/parts.md';
import CustomProps from '@ionic-internal/component-api/v8/segment/custom-props.mdx';
import Slots from '@ionic-internal/component-api/v8/segment/slots.md';

<head>
  <title>ion-segment: API Documentation for Segmented Controls</title>
  <meta name="description" content="ion-segments display a group of related buttons—sometimes known as segmented controls. View our Segment API Documentation to learn more about usage." />
</head>

import EncapsulationPill from '@components/page/api/EncapsulationPill';

<EncapsulationPill type="shadow" />


Segments display a group of related buttons, sometimes known as segmented controls, in a horizontal row. They can be displayed inside of a toolbar or the main content.

Their functionality is similar to tabs, where selecting one will deselect all others. Segments are useful for toggling between different views inside of the content. Tabs should be used instead of a segment when clicking on a control should navigate between pages.


## Basic Usage

Segments consist of [segment buttons](./segment-button) with a `value` property on each button. Set the `value` property on the segment to match the value of a button to select that button. Segments can also be disabled to prevent users from interacting with them.

import Basic from '@site/static/usage/v8/segment/basic/index.md';

<Basic />


## Scrollable Segments

Segments are not scrollable by default. Each segment button has a fixed width, and the width is determined by dividing the number of segment buttons by the screen width. This ensures that each segment button can be displayed on the screen without having to scroll. As a result, some segment buttons with longer labels may get cut off. To avoid this we recommend either using a shorter label or switching to a scrollable segment by setting the `scrollable` property to `true`. This will cause the segment to scroll horizontally, but will allow each segment button to have a variable width.

import Scrollable from '@site/static/usage/v8/segment/scrollable/index.md';

<Scrollable />


## Segments in Toolbars

<!-- Reuse the playground from the Toolbar directory -->
import Toolbar from '@site/static/usage/v8/toolbar/segments/index.md';

<Toolbar />


## Swipeable Segments

Each [segment button](./segment-button.md) can be associated with a [segment content](./segment-content.md) element that will be displayed
when the segment is active. With this approach, each segment's content can be swiped or scrolled between and the segment will be updated
to reflect the currently visible content.

:::warning
If no initial `value` is assigned to the `ion-segment` when using swipeable segments, the segment will default to the value of the first segment button.

Segment buttons cannot be disabled when used with swipeable segments.
:::

import Swipeable from '@site/static/usage/v8/segment/swipeable/index.md';

<Swipeable />

## Theming

### Colors

import Colors from '@site/static/usage/v8/segment/theming/colors/index.md';

<Colors />

### CSS Custom Properties

import CSSProps from '@site/static/usage/v8/segment/theming/css-properties/index.md';

<CSSProps />


## Accessibility

### Keyboard Interactions

The component has full keyboard support for navigating between and selecting `ion-segment-button` elements. By default, keyboard navigation will only focus `ion-segment-button` elements, but you can use the `selectOnFocus` property to ensure that they get selected on focus as well. The following table details what each key does:

| Key                                  | Description                                    |
| ------------------------------------ | ---------------------------------------------- |
| <kbd>ArrowRight</kbd>                | Focuses the next focusable element.            |
| <kbd>ArrowLeft</kbd>                 | Focuses the previous focusable element.        |
| <kbd>Home</kbd>                      | Focuses the first focusable element.           |
| <kbd>End</kbd>                       | Focuses the last focusable element.            |
| <kbd>Space</kbd> or <kbd>Enter</kbd> | Selects the element that is currently focused. |

## Interfaces

### SegmentChangeEventDetail

```typescript
interface SegmentChangeEventDetail {
  value?: string;
}
```

### SegmentCustomEvent

While not required, this interface can be used in place of the `CustomEvent` interface for stronger typing with Ionic events emitted from this component.

```typescript
interface SegmentCustomEvent extends CustomEvent {
  target: HTMLIonSegmentElement;
  detail: SegmentChangeEventDetail;
}
```


## Properties
<Props />

## Events
<Events />

## Methods
<Methods />

## CSS Shadow Parts
<Parts />

## CSS Custom Properties
<CustomProps />

## Slots
<Slots />
