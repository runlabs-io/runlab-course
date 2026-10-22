# What a lab is made of

The lab you just took is a folder with a file in it.
That is all a lab needs.
In this lab you will make one, right here in the terminal.

## A folder with a lesson

A lab is a folder. The folder's name is the lab's name.
Inside it, a file called `index.md` is the lesson, written in Markdown.

Make a folder and write the smallest lesson there is:

```shell
mkdir -p mylab
printf '# Hello\n\nThis is my first lab.\n' > mylab/index.md
```

Look at what you made:

```shell
ls mylab
cat mylab/index.md
```

The `#` line is a heading, and the rest is a paragraph.
Those two lines are a complete lab.
Everything you have been reading is this same kind of file, with more in it.

## A title for the catalog

A second file is optional: `config.yaml`.
It holds the lab's **title** and **description**, which is what the catalog shows before someone opens the lab.

```shell
printf 'title: Hello\ndescription: My first lab.\n' > mylab/config.yaml
cat mylab/config.yaml
```

That is two files and about five lines.
Later labs add one idea at a time: blocks that run commands, a terminal split in two, a web page you can open.
You can stop at any point and have a working lab.

## Finish

Press **Complete lab** when you are ready.
