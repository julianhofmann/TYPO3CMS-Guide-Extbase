.. include:: ../../Includes.txt

.. highlight:: html

.. _viewhelper-variable:

f:variable
==========

This ViewHelper was introduced in v8.6 to assign one template variable which will exist also after the ViewHelper is done rendering, i.e. adds template variables.

If you require a variable assignment which does not exist in the template after a piece of Fluid code is rendered, consider using `f:alias` instead.

Properties
==========

name
----

:aspect:`Variable type`
    String

:aspect:`Description`
    Name of variable to create.

:aspect:`Default value`

:aspect:`Mandatory`
    Yes


value
-----

:aspect:`Variable type`
    Mixed

:aspect:`Description`
    Value to assign. If not in arguments then taken from tag content.

:aspect:`Default value`

:aspect:`Mandatory`
    No

Examples
--------

Tag notation

::

   <f:variable name="myvariable">some value</f:variable>
   <f:variable name="myvariable"><f:format.htmlspecialchars>{oldvariable}</f:format.htmlspecialchars></f:variable>

Inline notation

::

   {f:variable(name: 'myvariable', value: 'some value')}
   {oldvariable -> f:format.htmlspecialchars() -> f:variable(name: 'newvariable')}


