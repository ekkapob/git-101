# Workshop 1
### Prerequisites
- Git installed
- Have GitHub account
- Link commputer SSH key with GitHub's account
  1. [New SSH Key](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
  2. [Add SSH to GitHub](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)

### Objective
![Objective](https://user-images.githubusercontent.com/710161/159395741-19eeaa7f-ef33-4a86-b9de-96b810a7d6a7.jpg)


### Preparation Steps
1. Team up with 3-4 developers
2. Nominate a lead developer (whose GitHub's repository will be used as the main)
3. For lead developer,
    1. Create a public repository `git-101`
    2. Add other developers' GitHub accounts as `git-101` repository collaborators
    3. Create a branch protection rule on 'main' branch, to have "Require a pull request before merging"
    ![branch protection](https://user-images.githubusercontent.com/710161/158508423-15b80046-8cc8-4843-ac05-0a08d284eaf9.png)
4. For other developers (the collaborators)
    1. After the lead developer invites to be the repo collaborator, check email (registered with GitHub) and "Accept" the inivitation

### The Work
#### Objective:
- Learn Git collaboration flow including Push, Pull, Code Review, Resolve Conflicts, Merge, Delete, and etc.

#### The Final Result:
File: `workshop-1.txt` in `main` branch with accumulative content from _n_ developers
```
Hello World
Edited by Developer 1's nickname
Edited by Developer 2's nickname
Edited by Developer 3's nickname
Edited by Developer 4's nickname
...
```

#### Start

1. Lead developer commits and pushes a file `workshop-1.txt` with content "Hello World" to GitHub `main` branch
2. For Everyone,
    1. Clone `git-101` to their local repo
       
       ```
       $ git clone {the leader's repository i.e. git@github.com:ekkapob/git-101.git}
       ```
       
    2. Create a branch with a name of individual's nickname e.g. ek, jack, jane.

       ```
       $ git checkout -b {branch name}
       ```

    3. Switch to work in `#2` branch. Normally, you are automatically switched to new branch after step 2. You can check that you are on the `#2` branch by.
       ```
       $ git status
       On branch ek <-- this should be the #2 branch you created.
       ...
       ```
    4. Edit `workshop-1.txt` by appending a line with "Edited by _{Your nickname}_"
    5. Commit the change and push to `git-101` with `#2` branch

       ```
       $ git add workshop-1.txt
       $ git commit -m "add line by {your name}"
       $ git push origin {branch name}
       ```

    6. Go to GitHub at `git-101` repo, create a pull request, assign a team member be a reviewer
    ![pull request](https://user-images.githubusercontent.com/710161/158511505-bad13040-d09d-4132-930e-7fd218300773.png)

3. For #6 reviewer,
    1. Go to GitHub at Pull Request
    2. Review the change
    ![Review](https://user-images.githubusercontent.com/710161/158512373-8a65a7eb-8e22-422c-97b1-68850bded880.png)
    3. Approve the change
    ![Approved](https://user-images.githubusercontent.com/710161/158512668-7cc2a6e5-70cf-4b5a-8fdc-ecee417d552f.png)
    4. Merge the change into `main` branch
    ![Merged](https://user-images.githubusercontent.com/710161/158512793-b10c514c-0558-4f20-ab54-12cc2984b96f.png)
    ![commit](https://user-images.githubusercontent.com/710161/158512895-fa712510-ba40-4d62-bbc8-a7fbdbd82685.png)
    5. Delete the _{nickname}_ branch
    ![delete branch](https://user-images.githubusercontent.com/710161/158512924-2949abce-ef6d-46ba-a53b-c9e2de20ecd2.png)

4. For #6 reviewer (with Conflicts)
    1. Resolve conflicts
      ![conflicts](https://user-images.githubusercontent.com/710161/158514138-e9cb73ba-1d91-454d-8fac-5571d8d9e802.png)
      ![solve conflicts](https://user-images.githubusercontent.com/710161/158514234-c28d4fa4-7a3a-49b2-bf01-0cf8eed321a6.png)
      ![solved](https://user-images.githubusercontent.com/710161/158515601-a6f07872-6dca-4d74-89d2-853240456c18.png)
      ![commit merge](https://user-images.githubusercontent.com/710161/158515652-a6383469-6818-4f73-a906-6cc48437446c.png)
    2. Approve, Merge change and Delete _{nickname}_ branch
      ![merge](https://user-images.githubusercontent.com/710161/158515997-3f138fb6-1f66-44b8-8a7d-1f4934084b48.png)

      

