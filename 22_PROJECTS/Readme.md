# PROJECTS

Github Projects is a planning and tracking tool when on working on Github Repo.

A project has an adaptable view that can be changed at anytime between:
- Spreadsheet (Table)
- Taskboard (Board)
- Roadmap (Roadmap)

Projects directly integrates with Issues and Pull Requests.

Project have build-in workflows to automate common actions.

## ABOUT PROJECTS

A project is an adaptable spreadsheet, task-board, and road map that integrates with your issues and pull requests on GitHub to help you plan and track your work effectively. 

You can create and customize multiple views by filtering, sorting, grouping your issues and pull requests, visualize work with configurable charts, and add custom fields to track metadata specific to your team. 

### Staying up-to-date

<ins>Your projects are built from the issues and pull requests you add, creating direct references between your project and your work.</ins>

> [!WARNING]  
> Must remember:
> - Information is synced automatically to your project as you make changes, updating your views and charts.
> - This integration works both ways, so that when you change information about a pull request or issue in your project, the pull request or issue reflects that information. 

### Adding metadata to your items
You can use custom fields to add metadata to your issues, pull requests, and draft issues and build a richer view of item attributes.

<ins>You’re not limited to the built-in metadata (assignee, milestone, labels, etc.) that currently exists for issues and pull requests.</ins>

For example, you can add the following metadata as custom fields:
- A date field to track target ship dates.
- A number field to track the complexity of a task.
- A single select field to track whether a task is Low, Medium, or High priority.
- A text field to add a quick note.
- An iteration field to plan work week-by-week, including support for breaks.

## LAYOUT OPTIONS
A project is componsed of multiple views, you can add more views to your project.

Each view's layout can be changed at anytime to accommodate the project use-case
- **Table**: This layout is great for your traditional ticket tracker and large amount of task
- **Board**: This layout is great for your agile tasks and understand clearly the state of issues
- **Roadmap**: This layout is great for planning based on a timeline

For your layout you can configure your data based on multiple options
- **Fields**: Add custom data fields to each project item (eg: status, assignees)
- **Column by**: Organize board columns based on specific fields (eg: status)
- **Group by**: Group by items into rows based on a chosen field (eg: assignee, label)
- **Sort by**: Define the order of items within columns or groups (eg: by priority)
- **Fields sum**: Show a summary or total of a particular field for all items in a column/group
- **Slice by**: Filter visible items on the board by specific field (eg: milestone, label)
- **Zoom level**: *(Roadmap only)* Adjust the view of the roadmap timeline (daily, monthly, quarterly)
- **Dates**: *(Roadmap only)* Set and view start and end date for each time on the roadmap

Remeber about items that:
- Your Github Project Items have custom fields
- You can create new fields
- Provide options to easily fill in the fields

## PROJECTS VS CLASSIC PROJECTS COMPARISON

Github Projects offers more advance and flexible project management tools compared to Github Classic Projects, which is simpler and more straightforward.

| Feature | Github Projects | Github Classic Projects |
| --- | --- | --- |
| Interface | New more dynamic interface with tables, board and views | Traditional board view similar to Trello |
| Flexibility | Highly customizable with different view and fiels | Limited customization options |
| Automation | Supports automated workflows and field updates | Basic automation capabilities |
| Reporting | Enhance reporting features and insights | Basic reporting and tracking |
| Integration | Deeper integration with Issues and Pull Requests | Basic integration with repositories |

## PROJECT OPTIONS

The configuration options for projects include creating a project, setting project descriptions and README, adding issues (including draft issues), creating custom fields (such as for tracking priority or iteration), grouping issues, saving views, adding board layouts, and configuring built-in automation workflows.

To create a project, users can choose between organization or user projects, then select a template or start from scratch. 

Descriptions and READMEs can be added to communicate project purpose and instructions. Issues and pull requests can be added manually or through automation. 

Custom fields like iteration and priority can be created to organize and track tasks effectively. Views can be saved and shared to maintain alignment on priorities. Board layouts can be utilized to visualize project progress based on status. Finally, built-in automation workflows can be configured to streamline project management tasks like auto-adding issues and setting statuses.

### Creating a project
1. Choose between organization or user project.
2. Select project type or template.
3. Enter project name and create.

### Setting your project description and README
1. Navigate to your project settings.
2. Add project description.
3. Update project's README with relevant information.

### Adding issues to your project
1. Paste issue or pull request URLs into the project.
2. Press Return to add.

### Adding draft issues to your project
1. Type draft issue idea and press Enter.
2. Add body text if needed.

### Adding an iteration field
1. Click on the rightmost field header and select "New field."
2. Type field name and select "Iteration."
3. Specify iteration duration and save.

### Creating a field to track priority
1. Click on the rightmost field header and select "New field."
2. Type field name and select "Single select."
3. Add priority options (High, Medium, Low) and save.

### Grouping issues by priority
1. Click on the view menu icon and select "Group."
2. Choose "Priority" to group issues.
3. Move issues between groups to change priority.

### Saving the priority view
1. Click on the view menu icon and select "Save changes."
2. Share the URL with your team to maintain alignment.

### Adding a board layout
1. Click "New view" and select "Board" layout.
2. Specify status for each issue.
3. Save changes and give the view a descriptive name.

### Configure built-in automation
1. Navigate to project workflows.
2. Edit "Auto-add to project" workflow to filter items.
3. Enable workflow to automatically add items.
4. Add a workflow to set status to Todo when an item is added.

## ADDING ITEMS TO A PROJECT

You have several options for adding issues and pull requests to your project. 

> [!IMPORTANT]  
> You can issues and pull requests to your project individually, automatically, or in bulk. 
> When you add an issue or pull request to your project, an event will be added to the issue or pull request's timeline.


<ins>Furthermore, you can include issues and pull requests from any organization, and you also have the ability to add draft issues that can be converted into regular issues later on.</ins>

### Automatically adding issues and pull requests
You can configure a built-in workflow to automatically add issues and pull requests from a repository when they meet specific filter criteria. 

### Pasting the URL of an issue or pull request

You can copy the URL of an issue or pull request into your clipboard and paste that into your project.

1. Place your cursor in the bottom row of the project, next to the <kbd>+</kbd>.
2. Paste the URL of the issue or pull request.
3. To add the issue or pull request, press <kbd>Return</kbd>

### Searching for an issue or pull request
If you know the issue or pull request number or if you know part of the title, you can search for an issue or pull request directly from your project.

1. Place your cursor in the bottom row of the project, next to the <kbd>+</kbd>.
2. To open the list of repositories, type <kbd>#</kbd>.
3. Select the repository where the pull request or issue is located. You can type part of the repository name to narrow down your options.
4. Select the issue or pull request. You can type part of the title to narrow down your options.

### Bulk adding issues and pull requests
You can add multiple issues and pull requests from your project and use filters, such as `label:bug`, to narrow down your search.

1. In the bottom row of the project, click <kbd>+</kbd>.
2. Click Add item from repository.
3. Optionally, to change the repository, click the dropdown and select a repository. You can also search for specific issues and pull requests.
4. Select the issues and pull requests you want to add.
5. Click **Add selected items**.


### Adding multiple issues or pull requests from a repository
You can also add issues and pull requests to your project from a repository's issue and pull request lists.

1. On GitHub.com, navigate to the repository that contains the issues or pull requests you want to add to your project.
2. Under your repository name, click <kbd>Issues</kbd> or <kbd>Pull requests</kbd>.
3. Select the issues or pull requests you want to add to your project.
    - To select individual issues or pull requests, to the left of the title of each issue or pull request you want to add to your project, select the checkbox.
    - To select every issue or pull request on the page, at the top of the list of issues or pull requests, select all.
4. Above the list of issues or pull requests, click <kbd>Projects</kbd>.
5. Click the projects you want to add the selected issues or pull requests to.

### Assigning a project from within an issue or pull request
You can also add an issue or pull request to your project from within the issue or pull request itself.

1. Navigate to the issue or pull request that you want to add to a project.
2. In the side bar, click **Projects**.
3. Select the project that you want to add the issue or pull request to.
4. Optionally, populate the custom fields.

### Using the command palette to add an issue or pull request
You can use the command palette when viewing your project to quickly add items.

1. To open the project command palette, press <kbd>Ctrl+K</kbd>
2. Start typing "Add items" and press Return.
3. Optionally, to change the repository, click the dropdown and select a repository. You can also search for specific issues and pull requests.
4. Select the issues and pull requests you want to add.
5. Click Add selected items.

### Creating issues
You can quickly create issues without leaving your project. When using a view that is grouped by a field, creating an issue in that group will automatically set the new issue's field to the group's value. For example, if you group your view by "Status", when you create an issue in the "Todo" group, the new issue's "Status" will automatically be set to "Todo."

1. At the bottom of a table, group of items, or a column in board layout, click <kbd>+</kbd>.
2. Click Create new issue.
3. At the top of the "Create new issue" dialog, select the repository where you want the new issue to be created.
4. Below the repository dropdown, type a title for the new issue.
5. Optionally, use the fields below the title field to set assignees, labels, and milestones, and add the new issue to other projects.
6. Optionally, type a description for your issue.
7. Optionally, if you want to create more issues, select Create more and the dialog will reopen when you create your issue.
8. Click Create.

Creating draft issues

Draft issues can have a title, text body, assignees, and any custom fields from your project. In order to populate the repository, labels, or milestones for a draft issue, you must first convert the draft issue to an issue. 

> [!IMPORTANT]  
> Draft issues are useful to quickly capture ideas. Unlike issues and pull requests that are referenced from your repositories, draft issues exist only in your project.

1. Place your cursor in the bottom row of the project, next to the .
2. Type your idea, then press Enter.
3.To add body text, click on the title of the draft issue. In the markdown input box that appears, enter the text for the draft issue body, then click Save.


## FIELDS

You can use text fields to include notes or any other freeform text in your project.

### Text and number fields

Text fields can be used in filters, for example: `field:"exact text"`. Text fields and item titles will also be used if you filter for text without specifying a field.

### Date fields
You can filter for date values using the YYYY-MM-DD format, for example: `date:2022-07-01`. 

<ins>If your project makes use of date fields, you can use the roadmap layout to view items on a timeline.</ins>

### Single select fields
You can create single select fields with multiple options, each with a description and a color, that can be selected from a dropdown menu.

You can filter by your single select fields by specifying the option, for example: `fieldname:option`.

You can filter for multiple values by providing a comma-separated list of options, for example: `fieldname:option1,option2`

Single select fields can contain up to 50 options.

### Iteration fields
You can create iterations to plan upcoming work and group items.

You can create an iteration field to associate items with specific repeating blocks of time. 

Iterations can be set to any length of time, can include breaks, and can be individually edited to modify name and date range.

With projects, you can group by iteration to visualize the balance of upcoming work, use filters to focus on a single iteration, and sort by iteration.

When you first create an iteration field, three iterations are automatically created. You can add additional iterations and make other changes on your project's settings page.

<ins>If your project makes use of iteration fields, you can use the roadmap layout to view items on a timeline.</ins>

### Tracks and Tracked by fields

You can view the subtasks of the issues in your projects.

You can enable the Tracks and Tracked by fields on your projects to see the relationships between your issues as you add subtasks in tasklists. 

The Tracked by field can be used to group items, creating a view that clearly shows the subtasks of each issue and the work required to complete them. 

You can also filter by the Tracked by field to display only items that are tracked by specific issues. Either start typing "tracked-by" and select an issue from the list or, if you know the repository and issue number, you can type the filter below in full. For example: `tracked-by:"<OWNER>/<REPO>#<ISSUE NUMBER>"`

### Delete and rename fields

You can delete and rename your custom fields under your repo project settings.

## AUTOMATING YOUR PROJECT
You have differents options to automate your projects.

> [!WARNING]  
> You must remember for the exam the following ones:
> - **Using the built-in automations**: You can use built-in workflows to automate your projects.
> - **Using the API to manage Projects**: You can use the GraphQL API to automate your projects.
> - **Automating Projects using Actions**: You can use GitHub Actions to automate your projects.
> - **Adding items automatically** You can configure your project's built-in workflows to automatically add items from repositories that match a filter.
> - **Archiving items automatically**: You can configure your project's built-in workflows to automatically archive items that match a filter.


## WORKFLOWS
Github built-in Projects Workflows allow you to automate what happens based on specific events.

You can find them on the 3 dots button <kbd>***</kbd> -> <kbd>Worflows</kbd>

> [!IMPORTANT]  
> Remember this built-in options:
> - Item added to project
> - Item reopened
> - Item closed
> - Code changes requested
> - Code review approved
> - Pull request merged
> - Auto-archive items
> - Auto-add to projects


**For more advanced automation of Github Projects you can use Github Actions**

## INSIGHTS

Projects insights lets you create charts about your Github Project

> [!IMPORTANT]  
> Remember there are 2 types:
> - **Current Charts**: Take a value and plot it (eg: how many items are assigned to each individuals)
> - **Historical Charts**: Take a value and plot over time (eg: track changes to the state of your project items)

## MANAGING SAVED REPLIES

When commenting on an issues or pull request, you can add a saved reply that you've already set up

### Creating a saved reply
If you frequently add the same comment over and over, you can create a saved reply.

1. In the upper-right corner of any page, click your profile photo, then click `Settings`.
2. In the "Code, planning, and automation" section of the sidebar, click `Saved replies`.
3. Under "Add a saved reply", add a title for your saved reply.
4. In the "Write" field, add the content you'd like to use for the saved reply.
5. To review your reply, click `Preview`.
6. Click Add saved reply.

### Editing a saved reply
You can edit the title and body of a saved reply.

1. In the upper-right corner of any page, click your profile photo, then click `Settings`.
2. In the "Code, planning, and automation" section of the sidebar, click  Saved replies.
3. Under "Saved replies," next to the saved reply you want to edit, click <kbd>Pencil Icon</kbd>.
4. Under "Edit saved reply," edit the title or content of the saved reply.
5. Click Update saved reply.

### Deleting a saved reply
If you find that you're no longer using a saved reply, you can delete it.
1. In the upper-right corner of any page, click your profile photo, then click `Settings`.
2. In the "Code, planning, and automation" section of the sidebar, click `Saved replies`.
3. Under "Saved replies", next to the saved reply you want to delete, click <kbd>X</kbd>.


## ASSIGNNING ISSUES AND PULL REQUESTS

You can assign issues and pull requests to specific users.

And filter Issues and PR based on the assignees.
