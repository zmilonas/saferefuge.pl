# Saferefuge.pl 

This is a simple static website about a Safe Refuge project.

This website uses [Hugo](https://gohugo.io/) - static site generator, and TailwindCSS as a css framework.

<img width="1220" alt="screenshot of saferefuge website in a web browser" src="https://user-images.githubusercontent.com/25948390/162583157-5549d381-1364-4300-915e-f3563dc471f9.png">

## Technology

File structure:

| Path                            | Description                                                          |
|---------------------------------|----------------------------------------------------------------------|
| `./content`                     | Pages written in markdown available under their respective `/` urls. |
| `./layouts/_default`            | templates for specific parts of the page                             |
| `./layouts/_default/index.html` | front page template                                                  |
| `./assets/css/input.css`        | main CSS file                                                        |
| `./static`                      | images and all other media files that should be deployed             |

The basic usage of the templates is using the Go (Go lang) templating engine. Here's an introduction from the Hugo team - [Introduction to Hugo Templating](https://gohugo.io/templates/introduction/)

## Running locally

Prequisites:

* [Hugo](https://gohugo.io/) - version v0.96.0 or higher
* [Node.js](https://nodejs.org/) - version can be matched to the `.node-version` file in the root of the project
* [Yarn](https://yarnpkg.com/) - Package manager for Node.js

First you need to install the dependencies:

    $ yarn install

Then to run the website you need to open **two terminal windows** and run 

    $ hugo serve

In the second one

    $ yarn tailwind --watch

This will allow you to work on the website by having a copy running on localhost:1313

Any changes should be immediately reflected.

This should be superseeded by a docker compose setup which will come later

## Deployment

The site is deployed with CloudFlare Pages, `yarn build` is ran on deploy and everything from the `./public` directory is served.

_Written by Zachary 10.04.2022_
