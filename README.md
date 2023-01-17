# Project Ideas App
A Daml backend designed for a platform for proposing project ideas to get rejected/approved.

### Overview 
This project was created by using the `empty-skeleton` template. The project adopts to exemplify the proposal-accept design pattern. A signatory can create a ProjectIdea contract. Then they can exercise the Propose choice as a controller to get the project proposal either approved or rejected by their manager. If the manager, a controller, exercises Reject choice on the proposed contract, the employee can exercise Revise choice on it to re-propose the project with updated details. Upon manager exercising Accept choice, a Project contract is created.

### Workflow
1. An employee creates a ProjectIdea contract. Both colleague and manager are invited as obeservers, but manager, as a controller, is authorized to exercise either Reject or Accept choices.
2. Upon the controller exercising Reject, a new contract is created.
3. Revise choice can be exercised on the newly generated contract from above.
4. Accept choice is exercised to finalize the project idea and generate a new Project contract.

### Building
To compile the project
```
$ daml build
```

### Testing
To test all scripts:
Either run the pre-written script in the `Test.daml` under /daml OR run:
```
$ daml start
```

### Running
To load the project into the sandbox and start navigator:
```
daml start
```