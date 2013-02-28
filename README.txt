CONTENTS OF THIS FILE
---------------------

  * Summary
  * Requirements
  * Installation
  * Configuration
  * Api functions
  * Credits


SUMMARY
-------

This module allows you to manage your google calendars.
Apis provided by module will allow you to create, update,
delete, fetch calendar details.
You can also create, update, delete, get, move a event from particular calendar.
You can fetch calendar settings, color details, etc.


REQUIREMENTS
------------
1. GAuth - Download it from http://drupal.org/project/gauth


INSTALLATION
------------

1. Copy this module directory to your sites/all/modules or
   sites/SITENAME/modules directory.

2. Install the required GAuth module.

3. Enable the module and manage accounts at
   admin/config/services/gauth_account.

4. Write own module to use apis of this module and manage calendar, events.



CONFIGURATION
-------------
1. Configure the api accounts at admin/config/services/gauth_account.

2. You can add new account or update existing accounts.
    Specify unique name by which you can identify the account.
    Add the client id, client secret and developer key from you google project
    page i.e. https://code.google.com/apis/console/
    Select Google Calendar services for which this account will be used.

3. On save of the form it will ask for access,
   click allow access so that the account gets authenticated.

4. Ready to use this account for api access.


 API FUNCTIONS
 -------------

1. gcal_calendar_create($calendar, $account)
   This function creates a google calendar

2. gcal_calendar_update($calendar, $account)
   This function updates a google calendar

3. gcal_calendar_delete($calendar_id, $account)
   This function deletes a google calendar

4. gcal_calendar_get($calendar_id, $account)
   This function fetches a array of google calendar details

5. gcal_calendar_public($calendar_id, $account)
   This function makes a existing calendar public

6. gcal_calendar_private($calendar_id, $account)
   This function makes a existing calendar private

7. gcal_setting_get($setting, $account)
   This function gets the setting value for the requested setting

8. gcal_setting_list($account)
   This function gets all settings for the account

9. gcal_colors_get($account)
   This function fetches all color ids.

10. gcal_event_create($event, $calendar_id, $account)
    This function creates a event on the specified calendar.

11. gcal_event_update($event, $calendar_id, $account)
    This function updates a event on the specified calendar.

12. gcal_event_delete($event_id, $calendar_id, $account)
    This function deletes a event on the specified calendar.

13. gcal_event_get($calendar_id, $event_id, $account)
    This function fetches a array of event details from the specified calendar

14. gcal_event_move($src_cal_id, $event_id, $dest_cal_id, $account)
    This function moves a event from one calendar to another calendar.

15. gcal_event_quickadd($calendar_id, 'Event title', $account);
    This function adds a event at current time by taking only the title of the event.

16. gcal_event_freebusy($params, $account);
    Returns free/busy information for calendar by searching event (find event).

17. gcal_acl_create($acl, $calendar_id, $account);
    This function creates a acl for the calendar.

18. gcal_acl_delete($calendar_id, $rule_id, $account);
    This function deletes a acl rule.

19. gcal_acl_get($calendar_id', $rule_id, $account);
    This function gets a acl rule setting.

20. gcal_calendarlist_create($callist, $account);
    This function creates a calendar list entry.

21. gcal_calendarlist_update($callist, $account);
    This function updates a calendar list entry.

22  gcal_calendarlist_get($calendar_id, $account);
    This function fetches a calendar list entry.

23. gcal_calendarlist_delete($calendar_id, $account);
    This function deletes a calendar list entry.

For more details of how to use these functions please refer EXAMPLES.txt file.
All api functions should be invoked using a account which is authenticated for
accessing calendar else will result in exceptions.
Ensure that you don't use the apis over the per day limit set by google
else enable billing.

CREDITS
-------

Current Maintainer: Sadashiv Dalvi <dalvisadashiv@gmail.com>
