<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" property="dct:title">Estimation Checklist</span> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.

As much as Agile discourages large up-front estimates they are still prevelant. Even the best most Agile-friendly clients need an understanding of scope-of-work before committing to work on a project.

This is **not** an estimation methedology or a replacement for good practices. iit is a simple collaborative checklist of questions that one should remember to ask when preforming such an estimation of a project or large-grained features. Some of these might not apply to you or have no answers, most should probably at least be discussed with the client.

Please fork, modify and PR to contribute!

- [ ] Is there an area for administrators? What goes in there?
  - [ ] Is there an area for super-users?
- [ ] What happens when entity X is deleted?
  - [ ] Can X even be deleted or just disabled? Is there a difference?
  - [ ] What happens to entities that reference X?
  - [ ] What happens to entities that X referenes?
- [] What is the CRUD workflow for each entity?
  - [ ] Which actions need approvals? How should approvals work?
  - [ ] Can any actions be un-done by the user?
  - [ ] Can users save drafts of updates? How does this interact with approvals, deletions & access?
- [ ] What are system/browser requirements? 
  - [ ] Can there be different ones for users in different roles? (eg admins will always use chrome latest)
  - [ ] What are the expectations for offline functionality?
- [ ] How will authentication work?
  - [ ] Will users register themselves for the system?
    - [ ] Can anyone register or do you need an invite?
    - [ ] Will this change over time? (eg beta invites)
    - [ ] Who sends invites? Where is the UI for this?
  - [ ] Is Oauth integration necessary? (eg Facebook or Google) Mandatory? (This can be great as then you don't have to store account info at all)
  - [ ] How will [forgotten usernames/passwords be handled?](http://www.troyhunt.com/2012/05/everything-you-ever-wanted-to-know.html)?
- [ ] What are the different usage roles within the system? (eg super-admin, manager, registered user, guest) 
  - [ ] How are authorization permissions assigned and managed? 
    - Which users should have access to which functionality?
    - Which users should have access to which data? (eg. a sales rep can't access notes on leads of other sales reps)
  - [ ] Which portions of the application are publically accessible?
- [ ] How often will a given page realistically be accessed? (especially important for pages containing lots of dynamic data)
- [ ] What is the infrastructure for deploying the application?
  - [ ] Who will support the deployment? What is their skillset?
  - [ ] Are there limitions on technology imposed by the client's infrastructure/team?
  - [ ] How will the application be deployed initially?
  - [ ] How will updates to the application be delivered? By whom?
  - [ ] Who will handle setting up an SSL certificate?
  - [ ] How should application health be monitored?
- [ ] What are any integration points?
  - [ ] What external systems must this application recieve messages from?
  - [ ] What external systems must this application send messages to?
    - [ ] Are there downloads that must be in any particular format?
- [ ] How will migration from existing systems work?
  - [ ] How will data be imported into the system upon launch?
  - [ ] What is the strategy if we have to roll back to the old system after launch? (eg due to bugs)
  - [ ] If we roll back, how will any data entered into the new system be pushed back into the old system?
- [ ] What sorts of reports should be available?
  - [ ] Which reports are available to each role?
  - [ ] How often will each report be run?
  - [ ] How up-to-date must each report be? (eg is containing day-old stale data ok?)
  - [ ] What format must each report be available in? (eg html, csv, xls, pdf)
  - [ ] Will these reports be imported into another system?
  - [ ] What sort of analytics and user-tracking information is required?
    - [ ] How should this information be accessible?
- [ ] For screens showing large amounts of data, must it be possible to display details of old data or is reporting sufficient for this?
- [ ] What personal information will be stored?
  - [ ] Is some data protected by PCI or HIPAA?
  - [ ] What information must be taken extra care with? (eg a system which stores names and addresses especially of minors)
- [ ] How long are you expected to support bugs?
- [ ] Who will handle user support and questions?
  - [ ] How exactly will users get in touch with support?
- [ ] Which features exactly are necessary for MVP?
  - [ ] Is it possible to get the core functionality prototyped in a few weeks with some scripts/Excel macros/etc?
  - [ ] How fancy do UI controls need to be? (eg can you just use built-in HTML5 browser validation)
- [ ] What are expectations for timelines?
  - [ ] When would you like MVP to launch?
  - [ ] Are there constraints by which MVP *must* launch? (eg the old system becomes deprecated in August)
  - [ ] When would you like there to be be a Beta launch? What should go into it over MVP?
  - [ ] When would you like the application to go public?
- [ ] Are users uploading files?
  - [ ] What are expectations for typical and maximum file size? How much storage must be available in the foreseeable future?
  - [ ] What is the expected frequency of downloads?
  - [ ] How fancy does the upload and download functionality have to be?
