# hcagent
A multi-agent Holochain system

# Introduction
`hcagent` extends Holochain to allow multiple agents on the same machine.

## Run your app on two browser tabs that simlulate two users
You've written the code and want to see if the app works for two users!

For that, we need to run two totally seperate instances of the app. Those instances are called a **node** or an **agent**.

To make it clean and simple, we will have two terminal windows open and run commands for every `agent` in its own terminal.

### Bite 1
Let's **create two agents** first and call them `a1` and `a2`:

*Terminal 1:* `$ hcagent init Jane`

*Terminal 2:* `$ hcagent init Alexar`

### Bite 2
Now, let's **install our app** for both of them:

*Terminal 1:* `$ hcagent as Jane hcadmin join ~/dev/mydapp/ mydapp`

*Terminal 1:* `$ hcagent as Alexar hcadmin join ~/dev/mydapp/ mydapp`

### Bite 3
Ok, ready to run the app?

Before we do so, we need to start the **Bootstrap Server (BS)**.

We need to keep Bootstrap Server running, so let's run it in a separete terminal:

*Terminal 3:* `$ bs --port=5001`

`bs` is a standard Holochain command. `hcagent` is using `5001` as the BS port.

### Bite 4

Finally it's time to run our apps, or better to say to get our **agents run their node**!

*Terminal 1:* `$ hcagent as Jane hcd mydapp 3141`

*Terminal 1:* `$ hcagent as Alexar hcd mydapp 3142`

Cool, had fun? More journeyes to come, stay tuned!

*Tip:* Did you know you can **Star** and **Watch** a project on Github at the same time?!

# Installation, Manual, Contribution, etc
They're all in the oven, in the meantime, enjoy dapping with Holochain with the above entrees!

# History
This project has evolved from `hctools` project.
https://github.com/pendashteh/hctools
