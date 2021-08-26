# lti-challenge-response

This is an extension for [Learning Tools Interoperability](https://www.imsglobal.org/activity/learning-tools-interoperability).

This proposal seeks to secure the LTI 1.3 launch from a MITM attack
where the JWT is intercepted and transported to another browser and
submitted in that other browser.  This was the problem identified 
as part of the original LTI 1.3 development and the OIDC Connect and
OIDC login end point was added to the spec to solve this.  

OIDC Connect as we designed has become untenable inside of an iframe
because browser manufacturers have begun blocking all cookies in iframes.

This proposal adds a post-launch verification that the same user is sitting
at the browser *after* the JWT is received and signature checked.

This proposal reviews the current problems and proposes 
a solution to the problem.

## Documents

- [The LTI Challenge Response Specification](specification.md)


<!--- Temporary Setup-only Section --->
# Extension folder setup process

  - [x] Free space
  - [ ] Name the service/message/extension: `Proper Project Name`
  - [ ] Create a short name/code name: `proper-project`
  - [ ] Copy `proposals/a-template` directory to a new directory with the short name `proposals/proper-project`
  - [ ] In new proposal directory find & replace: `ProperProjectName` with the actual name
  - [ ] In new proposal directory find & replace: `ShortProjectName` with the actual short name
  - [ ] Add a short description of the proposal at the top of this readme
  - [ ] Update this readme with other details as needed
  - [ ] Update the table in `proposals/readme.md` with the snippet below this checklist
  - [ ] (process decision needed) - See `GitHub Workflow Decisions below`
  - [ ] Delete this setup section and move onto work steps :)

## Proposal readme table row

```md
| [LTI Challenge Response Identity Verification](https://github.com/IMSGlobal/lti-proposals/tree/main/proposals/lti-challenge-response/specification.md) | Proposal | Augment / Replace OIDC Connect with Challenge Response |
```
<!--- End Setup Section --->

### Current Status

Proposal

## Process

### Work steps

  - Update `specification.md` with the proposal
  - Push changes to `main` or feature branch `ShortProjectName` as appropriate
  - Discuss with LTI workgroup
  - Tag issues with `ShortProjectName`
  - Do work
  - GOTO 1

### Making Contributions

Explain Github workflow, or link to main spec's workflow docs.

#### Github Workflow Decisions

  - Just push proposals to `main` branch? 
  - Only on feature branch first? 
  - Allow both and do what's appropriate for that given proposal? 
    
There isn't a convenient way to have whole specs in PRs for comment when many spec iterations will exist.
Maybe all proposals live on feature branches and there is an open PR for the whole branch?
That's less convenient for browsing the various proposals.


### Documentation finalization steps

- [ ] Update `respec-support/contributors.js` 
- [ ] Update `respec-support/local-biblio.js` 
- [ ] Access respec document via `respec-support/specification-wrapper.html` (needs web server to work properly) 
- [ ] Clean up any respec errors in `specification.md` ([common markdown problems in respec](https://github.com/IMSGlobal/spec-central/blob/master/markdown-notes.md))
- [ ] Make sure the final respec formatting and structure works well for `specification.md`

