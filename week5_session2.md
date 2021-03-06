* Thursday 15:00 UTC session: [Thursday Zoom
  link](https://bham-ac-uk.zoom.us/j/85697917669?pwd=R09RRVoxSXl5YnVjVDVuN3NDM2lCdz09)
* Friday 18:00 UTC session: [Friday Zoom link](https://bham-ac-uk.zoom.us/j/82522323304?pwd=VjRRWDNkZjF5clBDd3FNNGJWcTUyZz09).

## Recording

[Friday session](https://bham-ac-uk.zoom.us/rec/share/Ui0ZvX3ECuNHdo9lEsB46OCseXlooVVTNUo26icFeHy-E7mjraLvFvo0HnbGa_XW.53OZKYPJPpnr8-1H?startTime=1651860322000)

## Schedule and plan

* Github workflow and the final project.

### Working with the template repo

Diagram of the workflow:

![](https://learn.nipraxis.org/asset-v1:nipraxis+Pilot+Spring_2022+type@asset+block@github_workflow.png)


Team leader:

0. Before you start, agree a team name with your team, and get your team
   members' Github usernames — e.g. `matthew-brett`.
1. Go to <https://github.com/nipraxis/diagnostics-template>
2. Open the Issues tab.  You can get there directly by appending `issues` to
   the URL, like this:
   <https://github.com/nipraxis/diagnostics-template/issues>
3. Make a "New Issue".
4. In the issue, ask for a new diagnostics repository for your team.  Specify
   a *name* for your team.
5. Wait for our response, on that issue.
6. You will get an email inviting you to a new repository named
   `nipraxis-spring-2022/diagnostics-<teamname>` where `<teamname>` is the
   name you specified in your issue.
7. Go to the link for your repository.  It will be of form
   `https://github.com/nipraxis-spring-2022/diagnostics-<teamname>`.
8. Make sure you know the Github usernames of your team members.
9. Go to the Settings tab.
10. Click on "Collaborators and Teams" on the left.
11. Click on "Add people".  Add the team members with whatever permissions you
    agree.  Maybe "maintain" is a good default.
12. Wait for your team members to accept their invitations.

Everyone (including the team leader):

1. You should get an invitation to your team repository.
2. Click on the link, that should be of form
   `https://github.com/nipraxis-spring-2022/diagnostics-<teamname>`, where `<teamname>` is your agreed team name.
3. Click on the "Fork" button near the top right of the screen.
4. Accept the defaults, click "Create Fork".
5. Now you should be at a new page, with URL of form:
   `https://github.com/<your-gh-user>/diagnostics-<teamname>` where `<your-gh-user>` is your Github username.
6. Click on the green "Code" button, select the "SSH" tab.  Copy the link
   there, which will be of form:
   `git@github.com:<your-gh-user>/diagnostics-<teamname>`.  If you haven't got
   SSH keys set up yet have a look at [setting up SSH keys on
   Github](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent).  If you really get stuck use the "HTTPS" tab and link instead of the "SSH" tab.
7. Open a terminal on your computer.  Change to a suitable directory to store
   your code.  Consider `cd $HOME/nipraxis` if you don't have a strong
   alternative preference.
8. Type a suitably modified version of this command: `git clone
   git@github.com:<your-gh-user>/diagnostics-<teamname>`, replacing the
   relevant parts with your username and your team name.  (If you had to use
   HTTPS above, modify the clone command here accordingly).
9. You should now have a local *clone* of your *fork*.
10. Change directory to the new cloned repository, with command of form `cd
    diagnostics-<teamname>`.
11. Add a new *remote* that points to the main "upstream" version of your team
    code, using a command of form: `git remote add upstream https://github.com/nipraxis-spring-2022/diagnostics-<teamname>`.
12. Check your remote worked with the command `git fetch upstream`.
13. Make a new feature branch `editing-readme`, with the command `git branch
    editing-readme`.
14. Checkout this branch with `git checkout editing-readme`.
15. Make sure you are up to date with the latest code from upstream with `git
    merge upstream/main`.  This may do nothing, if there are no new changes in
    the upstream `main` branch.
16. Use your text editor to make a change to the `README.md` file.
17. `git add README.md`
18. `git commit` (if you have your text editor set up correctly to work with
    Git) or `git commit -m 'Edit to README'` (if you do not).
19. Push up your changes to your *fork* with `git push origin editing-readme
    --set-upstream`.
20. Go to your fork URL (of form
    `https://github.com/<your-gh-user>/diagnostics-<teamname>`)
21. You should see a new green "Compare and pull request" button for your
    `editing-readme` branch. Click on that, fill in the description and submit the pull request.

The team leader should:

1. Go to the main repository page — of form
   `https://github.com/nipraxis-spring-2022/diagnostics-<teamname>`.
2. Select one or more of the Pull requests to merge, and merge it / them.

## Modules and testing

* [sys.path](https://textbook.nipraxis.org/sys_path)
* [assert](https://textbook.nipraxis.org/assert)
* [path manipulation](https://textbook.nipraxis.org/path_manipulation)
* [docstrings](https://textbook.nipraxis.org/docstrings)

### Reading and homework for next week

You should have received a pull request into your upstream repository.  Please check there for the homework.

If you do not see a pull request, please email
<mailto:matthew.brett@gmail.com>.

The pull request has instructions, and some more pages to read.

Your task:

* Merge the pull request.
* Go to your local clone of your fork.
* `git fetch upstream`
* `git branch fix-detectors upstream/main`
* `git checkout fix-detectors`

For instructions, look in the files:

* `findoutlie/spm_funcs.py`
* `findoutlie/detectors.py`

And then work on the code to run the given commands and fix the errors, until
you get `Tests passed` from both given commands (see instructions in the PR).

Now push, and make a pull request.   Work together to find the best solution, review the pull request, and merge it.

## That's it.

That's it for this session.
