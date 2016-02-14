<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Estimation Checklist</span> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

As much as Agile discourages large up-front estimates they are still prevelant. Even the best most Agile-friendly clients need an understanding of scope-of-work before committing to work on a project.

This is meant to serve as a simple collaborative checklist of questions that one should remember to ask when preforming such an estimation of a project or large-grained features. Some of these might not apply to you or have no answers, most should probably at least be discussed with the client.

Please contribute!

- [ ] Is there a area for administrators? What goes in there?
- [ ] What happens when entity X is deleted?
  - [ ] Can X even be deleted or just disabled? Is there a difference?
  - [ ] What happens to entities that reference X?
  - [ ] What happens to entities that X referenes?
- [ ] What are system/browser requirements? 
  - [ ] Can there be different ones for users in different roles? (eg admins will always use chrome latest)
- [ ] How will authentication work?
  - [ ] Will users register themselves for the system?
    - [ ] Can anyone register or do you need an invite?
    - [ ] Will this change over time? (eg beta invites)
    - [ ] Who sends invites? Where is the UI for this?
  - [ ] Will users log in via their own account?
  - [ ] Is Oauth integration necessary? (eg Facebook or Google) Mandatory? (This can be great as then you don't have to store account info at all)
  - [ ] How will [forgotten usernames/passwords be handled?](http://www.troyhunt.com/2012/05/everything-you-ever-wanted-to-know.html)?
- [ ] What are the different usage roles within the system? (eg super-admin, manager, registered user, guest) 
  - [ ] How are authorization permissions assigned and managed?
  - [ ] Which portions of the application are publically accessible?
- [ ] How often will a given page realistically be accessed? (especially important for pages containing lots of dynamic data)
- [ ] What is the infrastructure for deploying the application?
  - [ ] Who will support the deployment? What is their skillset?
  - [ ] Are there limitions on technology imposed by the client's infrastructure/team?
  - [ ] How will the application be deployed initially?
  - [ ] How will updates to the application be delivered? By whom?
