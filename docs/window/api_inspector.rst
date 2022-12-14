API Inspector
=============

Although not the most complex part of the RenderDoc's UI, this page details the features and functionality of the API Inspector.

UI Elements
-----------

The API Inspector is divided into two sections - the top section is the most common, detailing the API calls and all of their parameters.

If an action is currently selected in the :doc:`event_browser`, all the API calls between the previous action and this action will be shown - in other words if you select a draw, this may show several state-setting API calls binding shaders or resources before the draw. If an individual event is currently selected then that event's API call will be shown.

The bottom section is less commonly used but shows the callstack from user code into the API entry point, if such a callstack is available and the symbols are resolved. For more information check out the page on :doc:`../how/how_capture_callstack`.

API Calls
---------

This section lists the series of API calls made between the preceding action and the currently selected action. The current action is always the last element in this list and is highlighted in bold. By default it is also the selected element.

Each API call can be expanded to see the parameters that were passed to it, in the form that they were serialised out to the capture.

.. figure:: ../imgs/Screenshots/APIList.png

	API Calls: A list of API calls made up to the current action.

Callstack
---------

The callstack section can be expanded by double clicking on the separator and collapsed in the same way. Once open its size can be adjusted by clicking and dragging on the separator.

This section will either show "No callstack available" or "Need to resolve symbols" as appropriate when the callstacks aren't ready for display.

The callstack follows the currently selected API call in the other section, and will update both as that selected call change and as the current event changes (as this implicitly changes the API call selected to whichever the current action is).

For more information see :doc:`../how/how_capture_callstack`

.. figure:: ../imgs/Screenshots/CallstackPanel.png

	Callstack: The callstack in user code where this API call was made.
