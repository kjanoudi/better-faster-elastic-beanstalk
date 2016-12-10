better-faster-elastic-beanstalk
===============================

This collection of hooks for AWS Elastic Beanstalk node.js containers that was designed to dramatically reduce deployment times, avoid unnecessary rebuilding of node_modules, install any version of node.js, install global NPM modules and more.

This project demonstrates several tweaks to the standard node.js Elastic Beanstalk configuration to significantly reduce deployment times by avoiding unnecessary rebuilds of node_modules. 

## Main features

 1. Install ANY desired node.js version as per your env.config (including
    the most recent ones that are not yet supported by AWS EB)  — control your node.js version to avoid surprises with sudden AWS updates or compatibility issues.
 2. Avoid rebuilding existing node modules, including in-app
    node_modules dir  — dramatically speed up deployment.
 3. Install node.js globally (and any desired module as well), if your use-case requires so.

Please see the original discussion on StackOverflow to grasp the concept:
http://stackoverflow.com/questions/21200251/avoid-rebuilding-node-modules-in-elastic-beanstalk

__NOTE__: this respo is way ahead of the StackOverflow thread, and heavily customised for my own use-case. It still works as a charm though and saves a lot of time on each deployment. Feel free to look around, be inspired and find solutions for your problems in my code, but it is essential to fork this repo and  adapt it for your own needs.

## Usage

I have uploaded my own personal ebextensions folder for example use. I believe you can just copy and paste the entire folder, as I typically do
on my new projects. There should be no, or very few, changes required. Node version is defined at the top of the `env.config` file.


