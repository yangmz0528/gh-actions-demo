# Github Actions

## Activity 1a: Simple Workflow
1. Create a new git repository and push to github
2. Create github actions directory `.github/workflows`
3. Create workflow at `.github/workflows/demo.yml`
4. Commit, push and check the workflow execution status

## Activity 1b: Errored Workflow
Observe that when an error occurs (e.g. non-zero exit by a program), the workflow would halt
1. Add `Faking an error` as a step within the last workflow
2. Commit, push and check the workflow execution status
  - failed at `exit 1`
  - Error: Process completed with exit code 1.

## Activity 2a: Another Workflow and Another Branch
Create a second workflow that shows the contents of your readme
1. Create a workflow at `.github/workflows/demo-2.yml`
   - Copy the full contents of `demo.yml`
   - Change the name to `Demo Workflow #2`
2. Modify the workflow such that it will print (e.g. `cat` command) the contents of the `README.md` file
   - How many workflow runs have been triggered? Ans: 2 workflow runs will trigger if there is 2 workflow

## Activity 2b: Narrowing the Scope of Workflow Triggers
Filters can be used to control when your workflow should run
1. Back to the `main` branch
2. Modify the workflow at `.github/workflows/demo2.yml` such that it gets triggered upon a push to the `main` branch only
3. Commit, push and check the workflow executions status
   - number of workflow runs depends on how many workflow is created
   - workflow will still get triggered when you introduce a change to another branch 
 
