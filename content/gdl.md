# GUI Definition Language

## Page
## Region
## Form
## Atom Edit Widget
An AtomEdit can be used to display an instance of a particular atom type and to modify it. An AtomEdit can be read-only or editable. It is possible to switch dynamically between the two modes. For this the ReadOnly property of the  AtomEdit can be bound to a boolean expression.

Typical atom edit widgets consist of 2 regions. One that contains the caption and another that contains the text representation of the atom. 

## Layout
A layout defines the placement of child visuals within a parent visual.

The most common layout is a column. Each child is placed under its predecessor. The implementation of such a column can be a grid.  ateThere can be The children are placed o
The atom editors typically

Layout can be implicitly. The model does not contain layout information. The layout rules are implemented by the generated software.
Layout can also be explicitly modeled. One way to do this is via the addition of a layout attribute to the container elements. (This is inspired by the use of CSS classes in HTML.) Another way is the introduction of layout elements in the model.### Section