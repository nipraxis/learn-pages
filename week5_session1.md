## Recording

We will post this after the session.

## Schedule and plan

* @ mentions on Github.
* [On testing](https://textbook.nipraxis.org/on_testing)

### DVars and testing

We will be working with the [DVARS
metric](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5915574/).

The reference above defines DVARS as the "spatial root mean square".

It's a measure of the difference in the voxel values between two volumes.

Assume `this_vol` is one 3D array representing a volume, and `prev_vol` is
another 3D array representing a volume.  The DVARS difference between these two volumes is:

```{python}
vol_diff = this_vol - prev_vol
dvar_val = np.sqrt(np.mean(vol_diff ** 2))
```

* Go to your breakout rooms as usual.
* We will send a pull request to the Github repository of your project's
  upstream repository.
* A team member should merge the pull request on Github.
* The *driver* for your session should do the following steps, with the
  *navigators* instructing the driver what to do, and watching for (the
  inevitable) mistakes.
* The rest of the steps are for the *driver*.
* Start a terminal.
* Navigate to your Git working directory with something like `cd
  $HOME/Documents/nipraxis-work/diagnostics-<team_name>` where `<team_name>` is
  your team name.
* Fetch the new contents of the upstream repository with `git fetch upstream`.
*   Start a new branch to do a PR to the upstream repository with:

    ```
    git branch add-dvars upstream/main --no-track
    git checkout add-dvars
    ```

*   Run the test command:

    ```
    python3 -m pytest findoutlie/tests/test_dvars.py
    ```

    If you get an error `No module named pytest`, then run:

    ```
    python3 -m pip install pytest
    ```

    and try again.

*   You might consider also *installing* your new directory module
    `findoutlie`. To do this:

    ```
    # You may be able to omit the --user below
    python3 -m pip install --user flit
    python3 -m flit install -s
    ```

    Don't worry if this does not work, or is confusing.  We will come back to
    that later.

*   Read the files:

    * `findoutlie/metrics.py` and
    * `findoutlie/tests/test_dvars.py`

    and complete these to make the tests pass.

* **Hint 1** — one of the ways to write the `dvars` function in the most
  efficient way, would use ideas from [4D to 2D reshaping
  page](https://textbook.nipraxis.org/reshape_and_4d.html). You might also
  benefit from the `np.diff` function.

* When you have solved this, make a pull request to the upstream repository,
  and @ mention one of the instructors for a review.

### Voxel statistics

If we have time.

* Git / testing exercise at <https://github.com/nipraxis/pearson>.
* [Voxel time courses](https://textbook.nipraxis.org/voxel_time_courses).
* [Voxel correlation
  exercise](https://hub.nipraxis.org/hub/user-redirect/git-pull?repo=https%3A//github.com/nipraxis/voxel_correlation&subPath=voxel_correlation.ipynb)

## That's it.

That's it for this session.