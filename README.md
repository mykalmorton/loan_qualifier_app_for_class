# Project Title


# User Story

As a user, I need the ability to save the qualifying loans to a CSV file so that I can share the results as a spreadsheet.

# Acceptance Criteria

Given that I’m using the loan qualifier CLI, when I run the qualifier, then the tool should prompt the user to save the results as a CSV file.
Given that no qualifying loans exist, when prompting a user to save a file, then the program should notify the user and exit.
Given that I have a list of qualifying loans, when I’m prompted to save the results, then I should be able to opt out of saving the file.
Given that I have a list of qualifying loans, when I choose to save the loans, the tool should prompt for a file path to save the file.
Given that I’m using the loan qualifier CLI, when I choose to save the loans, then the tool should save the results as a CSV file.

---

## Technologies

Python , CLI

---

## Installation Guide

How to do it with just the command line

1. Create a new repository on GitHub and initialize it with a README file
2. Create a folder on your local machine
3. Open terminal and move to that folder $ cd FOLDER
4. Add the remote URL as origin $ git remote add origin https://github.com/mykalmorton/loan_qualifier_app_for_class.git
5. Now using the pull command, you can ‘pull’ down the README file onto the local folder $ git pull origin master
6. Add your current files in the local folder to the staging area $ git add –-all
7. Commit your changes $ git commit -m "your commit message e.g. First commit"
8. Push your changes to the master branch $ git push origin master

---

## Usage

   Create a user dialog that prompts the user for whether they want to save their qualifying loans.
   Use Questionary to prompt the user with .confirm.ask.
   
```
    ask_user_to_save = questionary.text("Do you want to save their qualifying loans [Yes] or [No]").ask()
    if ask_user_to_save == 'yes' or ask_user_to_save == 'YES' or ask_user_to_save == 'y':
    
```

   create a user dialog for the function that saves a CSV file.
   Questionary to prompt the user, and ask for the output file path.
   
```
        csvpath = questionary.text("Enter a file name (.csv):").ask()
        csvpath = Path(path, csvpath)
```
---

## Contributors

Michael Morton 

---

## License

When you share a project on a repository, especially a public one, it's important to choose the right license to specify what others can and can't with your source code and files. Use this section to include the license you want to use.
