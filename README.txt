$ Id:$
GCal

An implementation of the Google Calendar API for Drupal.

Author: Aaron Craig (software@aaroncraig.com)
Developed by: Evolving Design (evolving-design.com)

This module implements the API described here: http://code.google.com/apis/calendar/data/2.0/developers_guide.html

The module is intended to be used by other modules who want to import/export to Google calendars

THIS IS A WORK IN PROGRESS
If you're interested in getting involved in development, please contact info@evolving-design.com

The entire API hasn't been implemented yet.  Below, you may see the current state of development.

For those that don't want to read the list, you currently can:
Create / delete a calendar
Make a calendar public
Create / edit / delete an event
Retrieve events for a given date range

You may only authenticate using the ClientLogin protocol, which means collecting the username and password from the user and passing it to Google.  GCal uses SSL for this part.

Authenticating to the Calendar service
  1. AuthSub proxy authentication (not implemented)
  2. ClientLogin username/password authentication
  3. Magic cookie authentication (not implemented)

Specifying a version
  The module always specifies version 2

Retrieving settings (not implemented)

Retrieving calendar lists
  1. Retrieving all calendars (not implemented)
  2. Retrieving only calendars that a user owns (not implemented)

Managing calendars
  1. Creating new calendars
  2. Updating existing calendars
  3. Deleting calendars

Managing subscriptions to calendars
  1. Adding new subscriptions (partially implemented, you may make a calendar public)
  2. Updating calendar subscriptions
  3. Deleting subscriptions

Retrieving events
  1. Retrieving events without query parameters (not implemented)
  2. Retrieving an event again (not implemented)
  3. Retrieving events for a specified date range
  4. Retrieving events matching a full text query (not implemented)

Creating events
  1. Creating single-occurrence events
  2. Creating quick add events (not implemented)
  3. Creating Calendar Event Gadgets (not implemented)
  4. Creating recurring events

Updating events

Deleting events

Sharing calendars
  1. Retrieving access control lists (not implemented)
  2. Retrieving a rule (not implemented)
  3. Adding a user to an access control list (partially implemented, you may make a calendar public)
  4. Updating a user's role in an access control list (not implemented)
  5. Removing a user from an access control list (not implemented)

Additional operations
  1. Extended properties (not implemented)
  2. Reminders and Notifications (not implemented)
  3. Comments (not implemented)
  4. GeoRSS data (not implemented)

Improving performance
  1. Requesting a partial response (not implemented)
  2. Making a partial update (not implemented)
  3. Performing multiple operations with a batch request (not implemented)

