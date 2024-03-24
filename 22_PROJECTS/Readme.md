# PROJECTS

Github Projects is a planning and tracking tool when on working on Github Repo.

A project has an adaptable view that can be changed at anytime between:
- Spreadsheet (Table)
- Taskboard (Board)
- Roadmap (Roadmap)

Projects directly integrates with Issues and Pull Requests.

Project have build-in workflows to automate common actions.


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

To create a project, users can choose between organization or user projects, then select a template or start from scratch. Descriptions and READMEs can be added to communicate project purpose and instructions. Issues and pull requests can be added manually or through automation. Custom fields like iteration and priority can be created to organize and track tasks effectively. Views can be saved and shared to maintain alignment on priorities. Board layouts can be utilized to visualize project progress based on status. Finally, built-in automation workflows can be configured to streamline project management tasks like auto-adding issues and setting statuses.

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
