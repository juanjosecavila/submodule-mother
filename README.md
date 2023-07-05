# submodule-mother

DEMO MOTHER

#### git submodule ####

### Initial configuration - Adding a Submodule ###
- In root, register the new submodule
    - `git submodule add https://github.com/juanjosecavila/submodule-child submodule-child`
    - The latest submodule update from 'main'
- In root, create a commit and push with the added submodule
    - `git add .`
    - `git commit -m "Added submodule"`
    - `git push`

### Initial configuration - Cloning repo with an existing Submodule ###
- In root, after cloning a repo, initialize the existing submodule
    - `git submodule update --init --recursive`
    - This has the specific submodule reference, could be outdated

### Update Submodule from repo ###
- In the 'submodule-child' folder, create a commit and push with the updated submodule
    - `git add .`
    - `git commit -m "Updated submodule"`
    - `git push`
- In root, create a commit and push with the updated submodule reference
    - `git add .`
    - `git commit -m "Updated submodule reference"`
    - `git push`

### Update for other repos where Submodule is outdated ###
- In root, get latest Submodule updates
    - Option a, locally, doesn't fetch
    - `git submodule update`
    - Option b, fetch all submodule updates, doesn't merge if conflicts
    - `git submodule update --remote`
    - Option c, fetch all submodule updates and merge submodule references
    - `git submodule update --remote --merge`
    - Need to handle if conflicts
- In root, create a commit and push with the updated submodule reference
    - `git add .`
    - `git commit -m "Updated submodule reference"`
    - `git push`
