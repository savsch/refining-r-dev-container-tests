# Hard-2 Test Results

## Screenshot of the information messages shown when creating the workspace

(with debug mode enabled)

![image](screenshots/container-creation-logs.png)

The docker container:

![image](screenshots/docker-container.png)

---

## Screenshot after following the [Running R](https://contributor.r-project.org/r-dev-env/tutorials/running_r/) tutorial

![running-r](screenshots/running-r.png)

#### Screen Recording

<video src="./screenshots/running_r.mp4" controls width=500></video>
![running-R-screen-recording](screenshots/running_r.mp4)

---

## What works and what doesn't?

I was able to follow the [Running R](https://contributor.r-project.org/r-dev-env/tutorials/running_r/) tutorial without any hurdle.

I tried exploring an in-built dataset and made a few plots, and encountered no issues at all.

![image](screenshots/misc_usage.png)

The only issue I encountered is that the default library path (inside `usr`) is not writable by the ssh'ed-into user `vscode`, so a warning is shown for using a different library path while installing a package for the first time.

![image](screenshots/unwritable-default-library-path.png)


#### Update (this subheading was added after posting the link to this test result on the wiki page)

Playing around a little bit more, I found that some of the functionality (specifically, the `which_r` bash function included with the container) that is vscode-specific, also doesn't work in positron.
