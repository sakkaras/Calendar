MGC Graphical Calendars Library (CalendarLib) is a set of views and controllers for displaying and scheduling events on iOS.

![Day Planner View](CalendarDocs/DayPlannerView.jpg?raw=true "Day planner view")

![Month Planner View](CalendarDocs/MonthPlannerView.jpg?raw=true "Month planner view")

![Year Calendar View](CalendarDocs/YearView.jpg?raw=true "Year calendar view")

# Features #

- Create and schedule events with iCal-like views and controllers
- 3 kinds of views are available (a day planner view, a month planner view and a year view)
- Scroll infinitely through days / months, or restrict scrolling to a given date range
- Restrict range of displayed hours in the day planner view
- Page through weeks in the day planner view
- Use a standard view for event cells or create your own custom views
- Easily customize appearance and layout (date format, size of headers, number of visible days...)
- Create events by tap-and-hold on the view
- Drag-and-drop events to another date or time
- Scroll through days / months while dragging
- Specialized controllers for EventKit data source but can easily work with any custom event provider 
- Background event loading for the EventKit controllers
- Ability to show an activity indicator for days while events are loading
- Restrict ability to create or move events to certain dates through datasource protocol methods (currently only in day planner view)
- Zoom in/out the day planner view to increase or decrease the height of hour slots

# Compatibility #

iPad / iPhone with iOS 8 or higher.

# Installation #

## CocoaPods ##
    
The best way is to use [CocoaPods](https://cocoapods.org/pods/CalendarLib). Add the following line to your `Podfile`: 

	pod 'CalendarLib', '~> 1.0'

## The old way ##

If you don't want to use CocoaPods, you need to copy the content of the CalendarLib folder into your project, as well as the source of the two dependencies: [OSCache](https://github.com/nicklockwood/OSCache) and [OrderedDictionary](https://github.com/nicklockwood/OrderedDictionary).

# Getting started #

1.  If you want to use EventKit as a data source, create an instance of `MGCDayPlannerEKViewController` or `MGCMonthPlannerEKViewController`, or subclass them for your own needs.
	
	Don't forget to add the following frameworks to the project:
	
	- **EventKit.framework**
	- **EventKitUI.framework**
	
2.  If you want to use another event provider, subclass one of `MGCDayPlannerViewController` or `MGCMonthPlannerViewController` and implement the data source protocol methods.

3.  If you want to use a custom event cell, subclass `MGCEventView` or `MGCStandardEventView` and register the class with the day / month planner view.
	
See the demo project to get an idea of how to use the library.

Have a look at the CalendarDocs folder for (incomplete) documentation on the day planner view.

# License #

MGC Graphical Calendars Library is available under the MIT license. See the LICENSE file.
