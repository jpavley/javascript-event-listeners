javascript-event-listeners
==========================

Exploring JavaScript event listeners using a button, the addEventListener() function, the querySelector() function, and a message map.

* Everything is in one file right now: index.html.

* Tested with Chrome and Safari, assumes HTML5.

* GNU General Public License.

JavaScript Explanation
----------------------

* Line 117: The var captureFlag is set to false so that events will be not be "captured" by my listeners created with addEventListener(). I think it defaults to false so setting the flag to false redundant.
* Line 119: The var counter is a simple variable to hold the number of events processed by each of my listeners. This variable tells us the order in which events were fired and how many events were fired.
* Lines 122-130: The var messageMap is a JavaScript object that maps the name of an event to a cell in the "Events Fired" column using querySelector(). This messageMap saves me a ton of code to right and makes adding new events really easy.
* Lines 133 and 136: The var button is the button where all the fun happens. I transform the curser into a "pointer" when the user mouses into the button.
* Lines 138-142: Attaches a event listener to the button for each event in the messageMap. I use an anonymous function so that I can pass the event object as a param to the event handler function.
* Lines 146-154: The event handler function that updates the counter and the innerHTML of the "Events Fired" column based on the event type. When the user first mouses into the button the "Events Fired" column is cleared of old values.
* Lines 158-163: The clearAll function that removes all the values in the "Events Fired" column.

I did my best to write as little code as possible while still being readable. The for/in loop is not performant and if this were production code I would have to write it as an optimized backwards for loop. For this demo I'm not worried about old non-HTML5 compliant browsers.
