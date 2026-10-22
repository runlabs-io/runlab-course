# Build your own lab

You have now used everything a lab is made of.
The next step is to make one, on your own machine, and put it on runlabs.io.

## What you need

- A **Linux x86_64** machine with **KVM**, which means hardware virtualization is turned on.
  Labs run in microVMs, and `trylab` runs the same ones on your machine.
- Permission to run one command with `sudo`, once.

To check for KVM on your own machine (not in this lab), run this there:

```console
ls -l /dev/kvm
```

If the file exists, you have it.

## Get the author pack

The pack is one download: **trylab**, the program you run, and the scripts and example labs around it.
Get the latest release from the **Author pack** link at the top of runlabs.io, unpack it, and run, from the unpacked folder:

```console
./prereqs
```

It installs what a lab build needs (Packer, and a small helper that gives `trylab` the network access a lab needs).
It is safe to run twice.

## Run a lab

`trylab` runs a lab folder on your machine, the way a learner will see it:

```console
./trylab basics
```

Your browser opens the lab: the same page you are on now, with your own terminal.
The pack comes with three examples, `basics`, `docker` and `nginx`. Copy one to start your own, or make a folder with an `index.md`, as you did two labs ago, and run that: `./trylab path/to/yourlab`.

## Change and run again

Edit `index.md`, save, and run `trylab` on the folder again.
Add the things you learned here one at a time: a `shell` block, a `view` block, a layout with two panes, a service.
You never need to publish anything to try an idea.

## Publish

When a lab is ready:

1. Put the folder in a GitHub repository (a repository can hold many labs, one folder each).
2. Sign in to runlabs.io with Google and open your **Profile**.
3. Connect your repository there, refresh it, and publish the lab.

Published labs appear on the front page. A lab starts out unpublished, so nothing shows until you say so.

## Finish

That is the whole loop: write a folder, run it with `trylab`, push it, publish it.
Press **Complete lab** when you are ready, and then go make something.
