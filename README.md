# Template for MIDS-W203 Section Specific Repositories
Use this repository as a template to create your section sprecific course repositories. 

## How to Use the Template?
https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template

### Best Practices
To be consistent across sections, rename the newly generated repo as follows:

NUM = section no, i.e., 08

TERM = fa (fall), sp (spring), or su (summer)

YY = 20, 21, etc.

For an example, "section_08_fa_20" is a valid repository name.

## Github Actions
Any repository generated from this template will contain *Github workflows* to automate the following weekly routines: 
- Release weekly homework
- Release homework solution

### Initialization Steps: Access Key and Secrets
Here are the steps to activate and customize the actions for your section repo.
i. Create a personal access token (https://docs.github.com/en/github/authenticating-to-github/creating-a-personal-access-token).
   For step 6, a good descriptive name would be "W203 token". In step 7, select "repo". Generate the token, and make sure to have it copied to 
   the clipboard. We need it in the following step. 
ii. Go to your section repository, then *Settings* -> *Secrets*.
iii. Click on the "New Secret" button to create a new *secret variable* with the name *W203*. In the *value* field, paste the copied access token
   from step (i).

   **Note:** Your acceess token and this secret should be kept secret. Grant your students only read/write permission. They will not have
   access to the secret unless you give them admin rights.

### Customize the Jobs
Follow the steps to customize the scheduled actions in your section repo. 
1. Go to *.github/workflows/release_hw.yml*. Follow the instructions documented in the file to chage line #14 and #23.
2. Go to *.github/workflows/release_solution.yml*. Follow the instructions documented in the file to chage line #14 and #23.
