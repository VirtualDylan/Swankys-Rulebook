Review the agile sprint plan defined in:
./docs/features/{feature title}

After reviewing the sprint plan and create the following files (based on the number of required sprints):
./docs/features/{feature title}/sprintXX.md

Our goal is create a Sprint Plan that will be used to effectively track our feature implementation. YOU MUST prioritize simple, readable code with minimal abstraction—avoid premature optimization. 

Utilize the following sprint Template:

# Sprint Template
```
# Sprint XXX

Sprint Goals:
Status: 

# Sprint Scope and Background
	- {Scope}
	- {Main Objectives}
	- {Project relevancy}
	- {Business Value}

# Tracker
Number of Planned Tasks: (count)
Number of Completed Tasks: (count)
Bugs Identified: (count)
Tech Debt Identified: (count)


# Sprint Closure (to be modified after all tasks are completed)
## Commit Message
{Git Commit Title}
{Git Commit Description}

## Sprint Review
### Issues and Risks
{Describe any bugs or issues you found during your implementation that should be addressed.}

### Closing Notes
{Final thoughts about the sprint}

# Tasks

## Task 1 - {Description}
{Status}
{Ticket Type} 
{Task Summary}
{Task Details}
{Success Criteria}

### Sub Tasks
- [ ] {Task Description}
- [ ] ...

### Developer Notes


### Dependencies and Risks


## Task 2 .......
```
