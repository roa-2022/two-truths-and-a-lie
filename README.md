# Two Truths and a Lie

Let's get to know each other better! We'll play an icebreaker called Two Truths and a Lie, but instead of chatting in person, we're going to use git and GitHub to chat about what the lie is. **Read the instructions very carefully as you work through this exercise** and let a teacher know if you need clarifications.


## Setup

### 0. Cloning the repo and `git iam`
- [ ] Clone this repo and navigate to it
  <details style="padding-left: 2em">
    <summary>More about cloning</summary>

    In your browser find the clone URL in the sidebar and copy it. In your terminal, run the following command, replacing `CLONE_URL` with the URL you copied:

    ```shell
    cd ~/workspace
    git clone CLONE_URL
    cd two-truths-and-a-lie
    ```
 </details>

- [ ] Tell git who is driving, using `git iam`
  <details style="padding-left: 2em">
    <summary>More about <code>git iam</code></summary>

    This is how we credit commits under your name when you're working on an on-campus machine or (for online students) in VS Code LiveShare.
    
    * Online students, please install and configure `git-iam` (following the instructions in the `remote-git-iam` repo)
    * On the on-campus computers, `git-iam` is already set up for you
    * If you're working solo on your own machine, you will have configured git globally already, and you don't need `git-iam`

    ```shell
    git iam DRIVERS_GITHUB_NAME
    ```
 </details>

----
## Tell a lie

### 1. Make your changes
- [ ] Create a new branch named for you and your partner
  <details style="padding-left: 2em">
    <summary>More about branching</summary>
    
    To do this we use the `git branch` command. `git branch` on its own lists out all local branches, but when we give it an argument it creates a new branch. A new branch is a copy of the current branch with a different name.
    
    In your terminal, run the following command, replacing `partner1` and `partner2` with your name and your partner's name in any order you decide:

    ```shell
    git branch partner1-partner2      # e.g. emily-kelly
    git checkout partner1-partner2
    ```

  You could also do this in one step:

  ```shell
  git checkout -b partner1-partner2
  ```
  The result should be one new branch named after your pair.
  </details>

- [ ] Modify the file `two-truths.md` so that for each of you it contains your name, and three facts about you. One of these facts should be completely made up
  <details style="padding-left: 2em">
    <summary>Tip</summary>

    - You should remove the entries for Neil Armstrong and Buzz Aldrin. 
  </details>

### 2. Share your work

- [ ] Stage and commit your file to the project
  <details style="padding-left: 2em">
    <summary>More about staging and committing</summary>

    Use the following commands:

    ```shell
    git add .
    git commit -m "Added truths and lies"
    ```
  </details>

- [ ] Push your branch to GitHub
  <details style="padding-left: 2em">
    <summary>More about pushing</summary>

    ``` shell
    git push origin YourName-PartnersName
    ```
  </details>

----
## Find the Lie

### 3. Prepare to bust

- [ ] Find a pair to bust
  <details style="padding-left: 2em">
    <summary>More about pairing</summary>

    **On-campus students:** a teacher will guide you to find the cohort mates with whom you're going to play lie detector. Ask your teacher who you're busting!

    **Online students:** Post in the `general` channel in Discord when your branch is ready to be busted. When you select another pair's branch to bust, mark their Discord message with an emoji reaction.
  </details>

- [ ] Pull your cohort mates' branch from GitHub into your local repository
  <details style="padding-left: 2em">
    <summary>More about pulling</summary>

    ```shell
    git fetch
    git checkout THEIR_BRANCH
    ```
  </details>

- [ ] Create a new branch for your changes
  <details style="padding-left: 2em">
    <summary>More about branching (again)</summary>

    ```shell
    git checkout -b THEIR_BRANCH-busted
    ```

    What is the difference between this command and the one in the previous step?
    
    ```shell
    git --help checkout
    ```
  </details>

### 4. Bust some lies

- [ ] Open `two-truths.md` and add the word **LIE** to the line you think is a lie

- [ ] Stage the changed file and commit it
  <details style="padding-left: 2em">
    <summary>More about staging and  committing (again)</summary>

    ```shell
    git add two-truths.md
    git commit -m "Found the lie"
    ```
  </details>

### 5. Fun with Github

- [ ] Push this branch to GitHub
  <details style="padding-left: 2em">
    <summary>More about pushing (again)</summary>

    ```shell
    git push origin THEIR_BRANCH-busted
    ```
  </details>

- [ ] Submit a pull request on GitHub of your changes. Be sure the pull request is from `THEIR_BRANCH-busted` into `THEIR_BRANCH`
  <details style="padding-left: 2em">
    <summary>More about pull requests</summary>
    
    The top of your PR will look similar to this:

    ![Screenshot of the top of a Github pull request showing a PR from the "don-rich-busted" branch to the "don-rich" base branch](pull-request-example.png)

    **DO NOT MERGE YOUR PULL REQUEST INTO MAIN!!**

    Why not? What would happen if everyone merged their branches into `main`?

----
## Come Clean

Now it's time to come clean (or not).

### 6. Reviewing PRs

- [ ] Once someone has submitted a LIE pull request on your branch, comment on the pull request
  <details style="padding-left: 2em">
    <summary>More about reviewing</summary>

    You might leave a comment such as...

    * "Yep you got it" or
    * "Nope but perhaps you really meant to choose #1" or (if you're devious)
    * "Nope, keep guessing".

    In any case, close the pull request and make sure the target branch is the correct one, **not** `main`.

## Stretch

<details style="padding-left: 2em">
  <summary>More about stretch challenges</summary>

  If you finish the main challenge with time left over, try these activities to solidify what you learned:

  * Draw a diagram of the Git workflows you used in sections 0-5
  * Describe the workflow using your picture and words (i.e. not code) to your pair or a teacher
  * Make sure you understand all parts **completely**. You will be using this workfow extensively in the next nine weeks. Ask questions if anything is still unclear!
</details>

## Further reading

<details style="padding-left: 2em">
  <summary>More reading</summary>

  * [GitHub Help](https://help.github.com/)
  * [Learn Git Branching](http://pcottle.github.io/learnGitBranching/)
  * [Git Cheatsheet](http://byte.kde.org/~zrusin/git/git-cheat-sheet-medium.png)
  * [Git homepage](https://git-scm.com/)
  * [GitHub Hello World](https://guides.github.com/activities/hello-world/)
  * [Gitflow Workflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow)
</details>
