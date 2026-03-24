# MoreScore: A piano fingering application 

This repository is a hub for all things MoreScore, a project researched under the supervision of [Dr. Antonina Kolkolova](https://www.cs.mun.ca/~kol/).

## Where is the code?

Though the source code has not yet been made public, it will soon be made availible and open-source. Currently, I am working on choosing an appropriate license and finalizing the project code. Keep an eye on my github over the coming days!

## What is it?

A major technical challenge for a pianist learning a new piece is to decide which fingers to use to play each note. While any note can potentially be played with any of the ten fingers, some combinations of finger positions are much easier to perform than others. Thus, finding a good fingering is a recurring task for pianists and piano teachers, especially since the perceived difficulty of a fingering is affected by individual differences such as hand size. MoreScore uses a dynamic programming algorithm for computing an optimal polyphonic fingering given sheet music and individual parameters. The program takes a MusicXML file for a piano score and adds fingering annotations. In our tests, the resulting fingerings are similar to those produced by professional pianists.

## Can I use it now?

Yes! MoreScore is ready to use at https://morescore.andrewluther.ca/  

## How was it made?

MoreScore is a python application I developed which uses a dynamic programming algorithm to optimize a set of fingerings using various fingering penalty metrics. The only dependency is [music21](https://music21.org/music21docs/), which is a python library for processing and analyzing musicXML files. Otherwise, all python code was written and developed by me, with ideas and guidance provided by [Dr. Antonina Kolkolova](https://www.cs.mun.ca/~kol/), who supervised the project. 

Originally, I developed a frontend using [React](https://react.dev/) with a backend [flask](https://flask.palletsprojects.com/en/stable/) python server. Eventually, this stack became difficult to maintain, and I switched to [reflex](https://reflex.dev/) for the frontend. This was convenient because it meant the entire application was written in python, and it also (at the time) allowed us to deploy the application for free. Unfortunately, reflex eventually updated to limit memory usage for applications at the free tier, and was no longer suitable for this project.

Now, MoreScore is running on my personal [digitalocean droplet](https://www.digitalocean.com/products/droplets), hosted at https://morescore.andrewluther.ca/. It is packaged using [docker](https://www.docker.com/). My good friend [Jack Harrhy](https://github.com/jackharrhy/) developed a nicer frontend for the project, and guided me through the deployment process.

## Where did you get the MoreScore logo?

I commissioned [Andrew Gosse](https://andrewgossecomposer.com/) to design the MoreScore logo, and he did an excellent job!
