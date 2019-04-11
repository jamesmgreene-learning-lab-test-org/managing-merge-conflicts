## Step 3: Resolve more complex conflicts

Just like your first conflict, this pull request is already conflicted.

This time, however, I've made it a bit more complicated.

- Instead of one conflict, you get three!
- Instead of conflicts in one file only, you get two!  
- One of your files actually has some leftover merge conflict markers. This can happen if someone forgets to remove the markers while resolving a conflict.

### :keyboard: Activity: Resolve these conflicts

{% if preferences.gitTool == 'cli' %}
1. Checkout to the `add-experience` branch and ensure it is up to date:
    ```shell
    git checkout add-experience
    git pull
    ```
2. Merge the `master` branch into the `add-experience` branch. To ensure that you're working with an up to date copy of `master`, we'll use its remote tracking branch:
    ```shell
    git merge origin/master
    ```
3. In Git's response, you'll see two files with conflicts: `_data/experience.yml` and `_data/interests.yml`.
4. Open `experience.yml` in your text editor.
5. Notice there are two distinct sets of conflict markers. This is because multiple sections of the file were modified on both branches. Git identified the two changes within the file as two separate conflicts. Remove the conflict markers and pick your desired content. 
6. With the merge conflicts resolved and the markers removed in the `experience.yml` file, stage the file:
    ```shell
    git add _data/experience.yml
    ```
7. Open the next file in your text editor: `_data/interests.yml`.
8. This file has some extra merge commit markers. Select the Interests you would like to list. Remove the others and all the extra conflict markers.
9.  Close the file. Stage it and commit your changes:
    ```shell
    git add .
    git commit -m "merge master into add-experience"
    ```
11. Push your merged branches to GitHub:
    ```shell
    git push
    ```
{% elsif preferences.gitTool == 'desktop' %}
1. Checkout to the `add-experience` branch by clicking **Current branch**, and selecting `update-config`. 
1. Merge `master` into the `add-experience` branch by clicking **Current branch**, and selecting **Choose a branch to merge into update-config**. 
1. Select the `master` branch, and click **Merge master into update-config**.
1. You'll be prompted about the merge conflict, and asked if you'd like to resolve it in your default editor. Click the button to open the file in your default editor. 
1. This file has some extra merge commit markers. Select the Interests you would like to list. Remove the others and all the extra conflict markers.
1. Save and close the file.
1. Back in GitHub Desktop, click **Commit merge**.
1. Push your changes back to the remote by clicking **Push origin**.
{% else %}
1. Click **Resolve conflicts**.
1. On the left, you will notice two files listed: `_data/experience.yml` and `_data/interests.yml`. Let's start with `experience.yml`.
1. Notice there are two distinct sets of conflict markers. This is because multiple sections of the file were modified on both branches. Git identified the two changes within the file as two separate conflicts.
1. With the merge conflicts resolved and the markers removed in the `experience.yml` file, click **Mark as resolved**.
1. GitHub will present the next file with conflicts, `interests.yml`.
1. This file has some extra merge commit markers. Select the Interests you would like to list. Remove the others and all the extra conflict markers.
1. When you are finished, click **Mark as resolved**.
1. Click **Commit merge**.
{% endif %}
<hr>
<h3 align="center">Watch below for my response.</h3>
