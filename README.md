This is a list I had made a few years ago after having to switch from Azure DevOps Repos and its PR tooling to use GitHub's PR tooling, because my employer at the time felt GitHub was a better repo host.  Some of these are subjective and some overlap, a few of them can be solved by a chrome extension, and some have been fixed by GitHub after this list was created. It has been sent to GH Support as part of a support ticket, so none of this should be any surprise to them.

1. doesnt display the files changed to me in the order I need to see them, instead forcing me navigate up and down an infinity scrolling page
1. doesnt show files changed in any common, predictable, or reliable ordered way
1. doesnt have a way to view the whole file by default, or at least increase the number of lines presented before and after the changed section
1. doesnt show any part of larger files even if a change was made to them.  
1. makes it very difficult to find and view the contents of files that were marked as deleted
1. doesnt have any file tree or other navigational view  
 	a. There is a chrome extension for this
	b. A tree view was added to the PR tools
1. always word wraps code files in the diffs, and it can't be disabled
1. makes poor use of my horizonal screen space
 	a. There are a few chrome extensions that will give you this
	b. This may have been fixed
1. doesnt prevent the PR from being approved by someone else and then backdoor merged after you had started a review and had made some comments
1. has a "conversations" view that must be what its like to read the diary of a schizophrenic - stream of consciousness, interrupted randomly, with some parts omitted and some parts represented poorly.
1. doesnt display the important parts of the PR at the top of the screen or in an overview page; status checks, reviewer results, conflicts, etc. instead making us scroll all the way to the end of the conversation schizo-stream.
1. doesnt consistently show comments on prior commits when viewing later or all commits, often marking them as outdated and hiding them, except to display a useless "outdated" notice in the conversations view.
1. doesnt have a clean and easy way to see and navigate through the unresolved comments
	a. A dropdown has been added for this but was buggy AF last time I had to use it.
1. doesnt prevent others - specifically the submitter - from resolving your comments  
   	a. Neither does AzDO
1. doesnt have the notion of sharing ownership of the review with another reviewer (useful when you have devs in different time zones and schedules)
 	a. Neither does AzDO
1. doesnt have a way to approve per commit  
	a. Neither does AzDO
1. does not have status checks tied to the PR, they are instead tied to the branch/commit. This means that two PR's (one closed, new one opened) for the same branch/commit will share status checks
1. spams everyone with an email for each comment and action instead of batching them or sending a "Hey, there are comments on this PR you submitted"  
	a.  but cant re-send review request without close/reopen/draft toggling  
1. will sometimes show the wrong file as the previous version   
	a. to be fair this was analyzed extensively by GH support and found to be due to how git fails to record explicit user actions (like moving a file and editing it in the same commit) and instead makes an assumption on the history of a file (must have been a Delete + Add. In the case that begat this complaint, a user had edited FileA and renamed it to FileB, then edited FileC and renamed it as FileA. GH PR tools couldnt cope with this and showed the original FileA vs its new incarnation.
1. cant make a comment and suggest changes in a different part of a code file where someone may have missed them.
