# NOTIFICATIONS

In your Github account settings you have a Notifications tab to configure notifications options.

Every notification allow 3 actions:
- Mark as don
- Dont get anymore alerts for it
- Bookmark or save for later

## FILTER OPTIONS

You can filter notifications using a filter syntax.

The are predefined saved filters.

You can create more saved filters using the filter syntax.

You can group notifications threads by repo or date.

## MENTIONS IN THREADS

A mention is when someone use a @ followed by your username.

If someone mentions you in a thread that you can find these mention under the Mentioned Filters.

## NOTIFICATION INBOX

The notification inbox provides a chronological list of notification threads. This allow you to keep on top of all suscribed activities with associated Github repos.

You can access it in [https://github.com/notifications](https://github.com/notifications)

In the notification section are 3 main gruops:
- **Inbox**
- **Saved**
- **Done**

</ins>The notifications that appear can be switched between All and Unread<ins>

> [!TIP]
> You can **Group by date or repository** your notifications.

### Filters
The filters also appears in the notification inbox. Allowing to restrict the search and allowing to create more.

The defaul ones are:
- Assigned
- Participating
- Mentioned
- Team mentioned
- Review request

### Manage notifications

The are 3 options to manage your notifications:
- Notification settings
- Watched repositories
- Subscriptions

## NOTIFICATION WATCHING

You can watch repo's in order to get notified of activities.

Your own repos are already set as watching.

You can see a watching list under https://github.com/watching

## NOTIFICATION SUBSCRIPTIONS

Subscriptions allow you to follow activities for a specific PR or Issue. Yo can toggle it between subscribed or unsubscribed.

You can see all your subscriptions under Notifications https://github.com/notifications/subscriptions


> [!CAUTION]
> Remember and not mix:
> **Watching**: Its for repos, people, organizations
> **Notification subscriptions**: Its for especific Pull Request and Issues


## NOTIFICATION SETTINGS

Some important aspecto about the settings for notifications are:

### Default notification email
Choose where you'd like emails to be sent. You can add more email addresses. Use custom routes to specify different email addresses to be used for individual organizations.

Define which email direction is associate with notifications.

### Automatically watch repositories
When you're given push access to a repository, automatically receive notifications for it.

It can be toggle on or off.

### Automatically watch teams
Anytime you join a new team, you will automatically be subscribed to updates and receive notification when that team is @mentioned.

It can be toggle on or off.

### Watching
Notifications for all repositories, teams, or conversations you're watching.

Select:
- Email
- On Github
- Or both

### Participating, @mentions and custom
Notifications for the conversations you are participating in, or if someone cites you with an @mention. Also for all activity when subscribed to specific events.

Select:
- Email
- On Github
- Or both


### Customize email updates
Choose which additional events you'll receive emails for when participating or watching.

Select events:
- Pull Request reviews
- Pull Request pushes
- Comments on Issues and Pull Requests
- Includes your own updates

### Ignored repositories
You'll never be notified. View ignored repositories. Opens the https://github.com/watching list.

### Actions
Notifications for workflow runs on repositories set up with GitHub Actions.

Select notification channels
- On GitHub
- Email
- Only notify for failed workflows


### Dependabot alerts: New vulnerabilities
When you're given access to Dependabot alerts automatically receive notifications when a new vulnerability is found in one of your dependencies.

Select notification channels
- On GitHub
- Email
- CLI

### Email weekly digest
Email a weekly summary summarizing alerts for up to 10 of your repositories.

Select between:
- Don't send
- Send weekly
- Send daily

### 'Deploy key' alert email
When you are given admin permissions to an organization, automatically receive notifications when a new deploy key is added.

It can be toggle on or off.

## MANAGING SUBSCRIPTIONS

Managing your subscriptions on GitHub involves various methods to efficiently handle notifications.

### Choosing how to unsubscribe:
- Unsubscribing can be done either from your inbox or the subscriptions page.
- Additionally, you can unwatch repositories to stop receiving updates.

### Unsubscribing from notifications in your inbox:
- Navigate to the notifications inbox.
- Select the notifications you want to unsubscribe from.
Click on "Unsubscribe" to remove them from your inbox.

### Unsubscribing from notifications on the subscriptions page:
- Access the subscriptions page from the manage notifications dropdown.
- Choose the notifications you want to unsubscribe from.
- Click on "Unsubscribe" to stop receiving them.

### Unwatching repositories:
- Access the watched repositories page from the manage notifications dropdown.
- Decide whether to unwatch a repository completely or customize notifications.
- You can also choose to unwatch all repositories owned by a user or organization.

### Benefits and differences:
- Unsubscribing from the inbox allows for additional triaging options and custom filters.
- Unsubscribing from the subscriptions page provides more context about subscriptions and sorting options.

> [!NOTE]  
>Remember, instead of unsubscribing, you have the option to ignore a repository, but it's not recommended as you won't be notified if you're @mentioned.

## MANAGE NOTIFICATIONS FROM INBOX

Managing notifications from your inbox involves organizing and handling notifications efficiently on GitHub.

### About your inbox:
1. Your inbox displays all notifications that you haven't unsubscribed from or marked as Done.
2. It offers customization options like filters and grouping to tailor it to your workflow.

### Triaging options:
- You have several options to manage notifications:
    - Save: For reviewing later.
    - Done: Marks a notification as completed and removes it.
    - Unsubscribe: Stops notifications until you're @mentioned.
    - Read/Unread: Marks notifications as read or unread.
- These options can be accessed via the notification dropdown menu.

### Triaging multiple notifications at the same time:
- Select multiple notifications and use the dropdown menu to apply triage options simultaneously.

### Default notification filters:
- By default, your inbox filters notifications for assignments, participation, review requests, and @mentions.

### Customizing your inbox with custom filters:
- You can create up to 15 custom filters.
- Access filter settings from your inbox settings.
- Add a name and query for your filter, e.g., filter notifications by repository or reason.
- Click "Create" to save the custom filter.

### Custom filter limitations:
- Custom filters have limitations like not supporting full-text search and a maximum of 15 filters.
- Default filters and their order cannot be changed using custom filters.

### Supported queries for custom filters:
- Various queries are supported for custom filters, including filtering by repository, discussion type, reason, author, and organization.
    - Examples of supported queries include filtering by `repo:`, `is:`, `reason:`,` author:`, and `org:`.

### Dependabot custom filters:
- Specific custom filters are available for Dependabot alerts, including filtering for vulnerability alerts, security alerts, and notifications generated by Dependabot.

## FIND THREATS WHERE YOUR ARE @MENTIONED

Navigate to your inbox:
1. Click on the inbox icon in the upper-right corner of any page on GitHub.
    - Filter notifications by @mentions:
2. Use the query is:mention to filter notifications where you have been directly @mentioned.
    - Alternatively, you can look for notifications with the reason:mention query.
3. View @mentions:
    - Notifications filtered by @mentions will display threads where you have been specifically mentioned.

By following these steps, you can efficiently manage your notifications and easily find threads where you have been @mentioned.

## CUSTOM WORKFLOW FOR TRIAGE NOTIFICATIONS

By following these steps, you can tailor your notification triage workflow to efficiently manage your GitHub notifications.

### Starting your inbox triage:
- Before beginning, determine whether you want to address urgent updates first or clear distracting notifications.
- You can combine both approaches based on the volume of notifications.

### Checking your highest notification priorities:
1. Decide which notifications need immediate attention, considering factors like review requests and direct mentions.
2. Prioritize your review process, such as:
    - Reviewing pull requests with review requests.
    - Addressing direct mentions.
    - Handling team mentions.
    - Checking CI workflow failures for specific repositories.

### Following up on ongoing notification updates:
1. Focus on resolving previously blocked items.
2. Prioritize follow-ups, such as:
    - Addressing assigned issues and pull requests.
    - Reviewing saved notifications, especially unread ones, and removing irrelevant ones.

### Managing lower-priority notifications:
1. After addressing high-priority notifications, focus on lower-priority ones like participating notifications.
2. Consider actions like unsubscribing from notifications or marking them as Done if completed.
3. Decide whether you want future updates on certain issues or pull requests.

### Clearing your least important notifications:
1. Determine which notifications can be quickly triaged and removed.
2. Prioritize clearing notifications like participating notifications you can unsubscribe from or irrelevant repository updates.

## NOTIFICATION CONFIGURATION OPTIONS 
Choose the type of activity on GitHub that you want to receive notifications for and how you want these updates delivered.

You can receive notifications for activity on GitHub.com in the following locations:
- The notifications inbox in the GitHub.com web interface
- The notifications inbox on GitHub Mobile, which syncs with the inbox on GitHub.com
- An email client that uses a verified email address, which can also sync with the notifications inbox on GitHub.com and GitHub Mobile

<ins>Web and mobile notifications must be enabled in the notification settings.</ins>

### Benefits of the Notifications Inbox:
The notifications inbox offers specific options tailored to the GitHub notifications flow, such as triaging multiple notifications at once, marking notifications as done, saving notifications for later review, and more.

### Benefits of Using an Email Client for Notifications:
Using an email client allows for indefinite storage of notifications based on the client's capacity and provides flexibility in the types of notifications received.

### Participating and Watching Notifications:
Watching a repository subscribes to updates for activity in that repository, and notifications can be customized for each repository, specifying which types of events trigger notifications.

### Custom Email Notifications:
GitHub sends multipart emails containing both HTML and plain text copies of the content, allowing users to configure their email client to display the preferred format.

Default email addresses can be chosen to receive updates for conversations and activity on GitHub.com.

### Dependabot, Secret Scanning, and GitHub Actions Notification Options:
Notification settings can be configured for Dependabot alerts, secret scanning alerts, and GitHub Actions workflow run updates, including delivery method and frequency.

### Organization Notification Settings:
Organization owners can receive email notifications when members add new deploy keys to repositories and can customize email addresses for notifications from different organizations.

### Managing Notification Settings with GitHub Mobile:

GitHub Mobile allows users to enable push notifications for various events within the app and schedule when notifications are sent to the mobile device.
