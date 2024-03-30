# FILTER SEARCH AND SORT

To find detailed information about a repository on GitHub, you can filter, sort, and search issues and pull requests that are relevant to the repository. 

## FILTERING ISSUES AND PR

> [!WARNING]  
> This filter section is apply to issues and PR at the same time.

Issues and pull requests come with a set of default filters you can apply to organize your listings.

You can filter issues and pull requests to find:
 - All open issues and pull requests
 - Issues and pull requests that you've created
 - Issues and pull requests that are assigned to you
 - Issues and pull requests where you're @mentioned
 - *Or use the advance search syntax*

## BY ASSIGNEES
Once you've assigned an issue or pull request to someone, you can find items based on who's working on them.

Above the list of issues or pull requests, select the Assignee dropdown menu.

The Assignee drop-down menu lists everyone who has write access to your repository. Click the name of the person whose assigned items you want to see, or click Assigned to nobody to see which issues are unassigned.

## BY LABELS

Once you've applied labels to an issue or pull request, you can find items based on their labels.

Above the list of issues or pull requests, click Labels. In the list of labels, click a label.

## BY REVIEW STATUS
You can use filters to list pull requests by review status and to find pull requests that you've reviewed or other people have asked you to review.

You can filter a repository's list of pull requests to find:

 - Pull requests that haven't been reviewed yet
 - Pull requests that require a review before they can be merged
 - Pull requests that a reviewer has approved
 - Pull requests in which a reviewer has asked for changes
 - Pull requests that you have reviewed
 - Pull requests that someone has asked you directly to review
 - Pull requests that someone has asked you, or a team you're a member of, to review


## SORTING ISSUES AND PR
Filters can be sorted to provide better information during a specific time period.

You can sort any filtered view by:

 - The newest created issues or pull requests
 - The oldest created issues or pull requests
 - The most commented issues or pull requests
 - The least commented issues or pull requests
 - The newest updated issues or pull requests
 - The oldest updated issues or pull requests
 - The most added reaction on issues or pull requests


Above the list of issues or pull requests, select the Sort dropdown menu, then click a <kbd>sort</kbd> method.

To clear your sort selection, click Sort > Newest.

## ADVANCE SEARCH

You can use advanced filters to search for issues and pull requests that meet specific criteria.

The issues and pull requests search bar allows you to define your own custom filters and sort by a wide variety of criteria. You can find the search bar on each repository's Issues and Pull requests tabs and on your Issues and Pull requests dashboards.

### Search only issues or pull requests

By default, GitHub search will return both issues and pull requests. However, you can restrict search results to just issues or pull requests using the `type` or `is` qualifier.

| Qualifier | Example |
| :--- | :--- |
| <kbd>type:pr</kbd> |	`cat type:pr` matches pull requests with the word "cat." |
| <kbd>type:issue</kbd> | `github commenter:andresmup type:issue`  matches issues that contain the word "github," and have a comment by @andresmup. | 
| <kbd>is:pr</kbd> | `event is:pr` matches pull requests with the word "event." |
| <kbd>is:issue</kbd> | `is:issue label:bug is:closed` matches closed issues with the label "bug." |


### Search by the title, body, or comments
With the `in` qualifier you can restrict your search to the title, body, comments, or any combination of these. When you omit this qualifier, the title, body, and comments are all searched.

| Qualifier | Example |
| :--- | :--- |
| <kbd>in:title	</kbd> | `warning in:title` matches issues with "warning" in their title.|
| <kbd>in:body	</kbd> | `error in:title,body` matches issues with "error" in their title or body.|
| <kbd>in:comments	</kbd> | `shipit in:comments` matches issues mentioning "shipit" in their comments.|

### Search within a user's or organization's repositories

To search issues and pull requests in all repositories owned by a certain user or organization, you can use the `user` or `org` qualifier. To search issues and pull requests in a specific repository, you can use the `repo` qualifier.

If you have access to pull requests in more than 10,000 repositories, you will need to limit your search to a specific organization, personal account, or repository to see results.

| Qualifier | Example |
| :--- | :--- |
| <kbd>user:USERNAME</kbd> | `user:andresmup github` matches issues with the word "github" from repositories owned by @andresmup. |
| <kbd>org:ORGNAME</kbd> | `org:github` matches issues in repositories owned by the GitHub organization. |
| <kbd>repo:USERNAME/REPOSITORY</kbd> | `repo:andresmup/github-foundations created:<2024-03-01` matches issues from @andresmup's github-foundations project that were created before March 2024. |


### Search by open or closed state
You can filter issues and pull requests based on whether they're *open* or *closed* using the `state` or `is` qualifier.

| Qualifier | Example |
| :--- | :--- |
| <kbd>state:open</kbd> | `libraries state:open mentions:andresmup` matches open issues that mention @andresmup with the word "libraries." | 
| <kbd>state:closed</kbd> |` design state:closed in:body` matches closed issues with the word "design" in the body. | 
| <kbd>is:open</kbd> | `performance is:open is:issue` matches open issues with the word "performance." | 
| <kbd>is:closed</kbd> | `python is:closed` matches closed issues and pull requests with the word "python." | 


### Search for pull requests in the merge queue
You can also use the `is` qualifier to find pull requests that are queued to merge.

| Qualifier | Example |
| :--- | :--- |
| <kbd>is:queued</kbd> | `is:queued` matches pull requests that are currently queued to merge. |

### Search by the reason an issue was closed
You can filter issues based on the reason given when the issue was closed, using the `reason` qualifier.

| Qualifier | Example |
| :--- | :--- |
| <kbd>reason:completed	</kbd> | `libraries is:closed reason:completed` matches issues with the word "libraries" that were closed as "completed." |
| <kbd>reason:"not planned"</kbd> |	`libraries is:closed reason:"not planned"` matches issues with the word "libraries" that were closed as "not planned." |

### Filter by repository visibility
You can filter by the visibility of the repository containing the issues and pull requests using the `is` qualifier. 

| Qualifier | Example |
| :--- | :--- |
| <kbd>is:public</kbd> |`is:public` matches issues and pull requests in public repositories. |
| <kbd>is:private</kbd> |`is:private` cupcake matches issues and pull requests that contain the word "cupcake" in private repositories you can access. |


### Search by author
The `author` qualifier finds issues and pull requests created by a certain user or integration account.

| Qualifier | Example |
| :--- | :--- |
| <kbd> author:USERNAME</kbd> | `github author:andresmup` matches issues and pull requests with the word "github" that were created by @andresmup. |
| <kbd> in:body author:USERNAME</kbd> | `github in:body author:andresmup` matches issues written by @andresmup that contain the word "github" in the body. |
| <kbd>author:app/USERNAME</kbd> | `author:app/andresmup` matches issues created by the integration account named "andresmup". |
| <kbd> -author:app/USERNAME </kbd> |`-author:app/andresmup` matches issues created by any user other than the integration account named "andresmup". <ins>The minus sign, or dash character <kbd>-</kbd> before the qualifier signifies a logical NOT for the qualifier in the search query. </ins>|


### Search by assignee
The `assignee` qualifier finds issues and pull requests that are assigned to a certain user. 

| Qualifier | Example |
| :--- | :--- |
| <kbd> assignee:USERNAME </kbd> |`assignee:andresmup repo:libgit2/libgit2` matches issues and pull requests in libgit2's project libgit2 that are assigned to @andresmup.|


### Search by mention
The `mentions` qualifier finds issues that mention a certain user. 

| Qualifier | Example |
| :--- | :--- |
| <kbd> mentions:USERNAME</kbd> | `data mentions:andresmup` matches issues with the word "data" that mention @andresmup.|

### Search by team mention
For organizations and teams you belong to, you can use the `team` qualifier to find issues or pull requests that @mention a certain team within that organization. Replace these sample names with your organization and team name to perform a search.

| Qualifier | Example |
| :--- | :--- |
| <kbd> team:ORGNAME/TEAMNAME</kbd> |`team:jekyll/owners` matches issues where the @jekyll/owners team is mentioned.</kbd> |
| <kbd> team:ORGNAME/TEAMNAME</kbd> |`is:open is:pr	team:myorg/ops is:open is:pr` matches open pull requests where the @myorg/ops team is mentioned.</kbd> |


### Search by commenter
The `commenter` qualifier finds issues that contain a comment from a certain user.

| Qualifier | Example |
| :--- | :--- |
| <kbd> commenter:USERNAME</kbd> | `github commenter:andresmup org:github` matches issues in repositories owned by GitHub, that contain the word "github," and have a comment by @andresmup.|

### Search by a user that's involved in an issue or pull request
You can use the `involves` qualifier to find issues that in some way involve a certain user.

The `involves` qualifier is <ins>a logical OR between the `author`, `assignee`, `mentions`, and `commenter` qualifiers</ins> for a single user. In other words, this qualifier finds issues and pull requests that were either created by a certain user, assigned to that user, mention that user, or were commented on by that user.

| Qualifier | Example |
| :--- | :--- |
| <kbd> involves:USERNAME</kbd> |`involves:andresmup involves:andresmpaws` matches issues either @andresmup or @andresmpaws are involved in.|
| <kbd> in:body involves:USERNAME</kbd> |`NOT data in:body involves:andresmup` matches issues @andresmup is involved in that do not contain the word "data" in the body.|


### Search for my issues and pull requests
You can search for issues and pull requests you have created or have interacted with by following the desired qualifier with `@me`. Any qualifier that works with a username allows you to limit your search to issues and pull requests you created, are assigned, mentioned on, or are requested as a reviewer of.

| Qualifier | Example |
| :--- | :--- |
| <kbd> author:@me</kbd> |`author:@me` matches issues and pull requests you have authored.|
| <kbd> is:pr commenter:@me</kbd> |`is:pr commenter:@me` matches pull requests you have commented on.|

### Search for linked issues and pull requests
You can narrow your results to only include issues that are linked to a pull request by a closing reference, or pull requests that are linked to an issue that the pull request may close.

| Qualifier | Example |
| :--- | :--- |
|<kbd> linked:pr</kbd>|`repo:desktop/desktop is:open linked:pr` matches open issues in the desktop/desktop repository that are linked to a pull request by a closing reference.|
|<kbd> linked:issue</kbd>|`repo:desktop/desktop is:closed linked:issue` matches closed pull requests in the desktop/desktop repository that were linked to an issue that the pull request may have closed.|
|<kbd>-linked:pr</kbd>|`repo:desktop/desktop is:open -linked:pr` matches open issues in the desktop/desktop repository that are not linked to a pull request by a closing reference.|
|<kbd>-linked:issue</kbd>|`repo:desktop/desktop is:open -linked:issue` matches open pull requests in the desktop/desktop repository that are not linked to an issue that the pull request may close.|

### Search by label
You can narrow your results by labels, using the `label` qualifier. Since issues can have multiple labels, you can list a separate qualifier for each issue.

| Qualifier | Example |
| :--- | :--- |
|<kbd>label:LABEL</kbd>|`label:"help wanted" language:python` matches issues with the label "help wanted" that are in python repositories.|
|<kbd>in:body -label:LABEL label:LABEL</kbd>|`broken in:body -label:bug label:priority` matches issues with the word "broken" in the body, that lack the label "bug", but do have the label "priority."|
|<kbd>label:LABEL label:LABEL</kbd>|`label:bug label:resolved` matches issues with the labels "bug" and "resolved."|
|<kbd>label:LABEL,LABEL</kbd>|`label:bug,resolved` matches issues with the label "bug" or the label "resolved."|


### Search by milestone
The `milestone` qualifier finds issues or pull requests that are a part of a milestone within a repository.

| Qualifier | Example |
| :--- | :--- |
|<kbd>milestone:MILESTONE</kbd>|`milestone:"overhaul"` matches issues that are in a milestone named "overhaul."|
|<kbd>milestone:MILESTONE</kbd>|`milestone:"bug fix"` matches issues that are in a milestone named "bug fix."|

### Search by project
You can use the `project` qualifier to find issues that are associated with a specific `project`. You must search projects by the project number. You can find the project number at the end of a project's URL.

| Qualifier | Example |
| :--- | :--- |
|<kbd>project:PROJECT_NUMBER</kbd>|`project:github/57` matches issues owned by GitHub that are associated with the organization's project 57.|
|<kbd>project:REPOSITORY/PROJECT_NUMBER</kbd>|`project:github-linguist/linguist/1` matches issues that are associated with project 1 in @github's linguist repository.|

### Search by commit status
You can filter pull requests based on the status of the commits.

| Qualifier | Example |
| :--- | :--- |
|<kbd>status:pending</kbd>|`language:python status:pending` matches pull requests opened into Python repositories where the status is pending.|
|<kbd>status:success</kbd>|`is:open status:success import in:body` matches open pull requests with the word "import" in the body with a successful status.|
|<kbd>status:failure</kbd>|`created:2015-05-01..2015-05-30 status:failure` matches pull requests opened on May 2015 with a failed status.|


### Search by branch name
You can filter pull requests based on the branch they came from (the "head" branch) or the branch they are merging into (the "base" branch).

| Qualifier | Example |
| :--- | :--- |
|<kbd>head:HEAD_BRANCH</kbd>|`head:change is:closed is:unmerged` matches pull requests opened from branch names beginning with the word "change" that are closed.|
|<kbd>base:BASE_BRANCH</kbd>|`base:gh-pages` matches pull requests that are being merged into the gh-pages branch.|


### Search by language
With the `language` qualifier you can search for issues and pull requests within repositories that are written in a certain `language`.

| Qualifier | Example |
| :--- | :--- |
|<kbd>language:LANGUAGE</kbd>|`language:python state:open` matches open issues that are in python repositories.|

### Search for draft pull requests
You can filter for draft pull requests.

| Qualifier | Example |
| :--- | :--- |
|<kbd>draft:true</kbd>|`draft:true` matches draft pull requests.|
|<kbd>draft:false</kbd>|`draft:false` matches pull requests that are ready for review.|


### Search by pull request review status and reviewer
You can filter pull requests based on their review status *(none, required, approved, or changes requested)*, by reviewer, and by requested reviewer.

| Qualifier | Example |
| :--- | :--- |
|<kbd>review:none</kbd>|`type:pr review:none` matches pull requests that have not been reviewed.|
|<kbd>review:required</kbd>|`type:pr review:required` matches pull requests that require a review before they can be merged.|
|<kbd>review:approved</kbd>|`type:pr review:approved` matches pull requests that a reviewer has approved.|
|<kbd>review:changes_requested</kbd>|`type:pr review:changes_requested` matches pull requests in which a reviewer has asked for changes.|
|<kbd>reviewed-by:USERNAME</kbd>|`type:pr reviewed-by:andresmup` matches pull requests reviewed by a particular person.|
|<kbd>review-requested:USERNAME</kbd>|`type:pr review-requested:andresmup` matches pull requests where a specific person is requested for review. Requested reviewers are no longer listed in the search results after they review a pull request. If the requested person is on a team that is requested for review, then review requests for that team will also appear in the search results.|
|<kbd>user-review-requested:@me</kbd>|`type:pr user-review-requested:@me` matches pull requests that you have directly been asked to review.|
|<kbd>team-review-requested:TEAMNAME</kbd>|`type:pr team-review-requested:github/docs` matches pull requests that have review requests from the team github/docs. Requested reviewers are no longer listed in the search results after they review a pull request.|


### Search by when an issue or pull request was created or last updated
You can filter issues based on times of creation, or when they were last updated. For issue creation, you can use the `created` qualifier; to find out when an issue was last `updated`, you'll want to use the `updated` qualifier.


| Qualifier | Example |
| :--- | :--- |
|<kbd>created:YYYY-MM-DD</kbd>|`language:c# created:<2011-01-01 state:open` matches open issues that were created before 2011 in repositories written in C#.|
|<kbd>updated:YYYY-MM-DD</kbd>|`weird in:body updated:>=2013-02-01` matches issues with the word "weird" in the body that were updated after February 2013.|

> [!NOTE]  
> Everything related to date format is YYYY-MM-DD (year-month-day).

### Search by when an issue or pull request was closed
You can filter issues and pull requests based on when they were closed, using the closed qualifier.

| Qualifier | Example |
| :--- | :--- |
|<kbd>closed:>YYYY-MM-DD</kbd>|`language:swift closed:>2014-06-11` matches issues and pull requests in Swift that were closed after June 11, 2014.|
|<kbd>in:body closed:<YYYY-MM-DD</kbd>|`data in:body closed:<2012-10-01` matches issues and pull requests with the word "data" in the body that were closed before October 2012.|

### Search by when a pull request was merged
You can filter pull requests based on when they were merged, using the `merged` qualifier.

| Qualifier | Example |
| :--- | :--- |
|<kbd>language:LANGUAGE merged:<YYYY-MM-DD</kbd>|`language:javascript merged:<2011-01-01` matches pull requests in JavaScript repositories that were merged before 2011.|
|<kbd>in:title language:LANGUAGE merged:>YYYY-MM-DD</kbd>|`fast in:title language:ruby merged:>=2014-05-01` matches pull requests in Ruby with the word "fast" in the title that were merged after May 2014.|


### Search based on whether a pull request is merged or unmerged
You can filter pull requests based on whether they're merged or unmerged using the `is` qualifier.

| Qualifier | Example |
| :--- | :--- |
|<kbd>is:merged</kbd>|`bug is:pr is:merged` matches merged pull requests with the word "bug."|
|<kbd>is:unmerged</kbd>|`error is:unmerged` matches pull requests with the word "error" that are either open or were closed without being merged.|


### Search based on whether a repository is archived
The `archived` qualifier filters your results based on whether an issue or pull request is in an archived repository.

| Qualifier | Example |
| :--- | :--- |
|<kbd>archived:true</kbd>|`archived:true GNOME` matches issues and pull requests that contain the word "GNOME" in archived repositories you have access to.|
|<kbd>archived:false</kbd>|`archived:false GNOME` matches issues and pull requests that contain the word "GNOME" in unarchived repositories you have access to.|


### Search based on whether a conversation is locked
You can search for an issue or pull request that has a locked conversation using the `is` qualifier.

| Qualifier | Example |
| :--- | :--- |
|<kbd>is:locked</kbd>|`code of conduct is:locked is:issue archived:false` matches issues or pull requests with the words "code of conduct" that have a locked conversation in a repository that is not archived.|
|<kbd>is:unlocked</kbd>|`code of conduct is:unlocked is:issue archived:false` matches issues or pull requests with the words "code of conduct" that have an unlocked conversation in a repository that is not archived.|


## SHARING FILTERS

When you filter or sort issues and pull requests, your browser's URL is automatically updated to match the new view.

You can send the URL that issues generates to any user, and they'll be able to see the same filter view that you see.

For example, if you filter on issues assigned to andresmup, and sort on the oldest open issues, your URL would update to something like the following:

> /issues?q=state:open+type:issue+assignee:andresmup+sort:created-asc
