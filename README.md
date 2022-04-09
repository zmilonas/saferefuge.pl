# Saferefuge.pl 

This is a simple static website about a Safe Refuge project.

This website uses Hugo - static site generator, and TailwindCSS as a css framework.

<img width="1220" alt="screenshot of saferefuge website in a web browser" src="https://user-images.githubusercontent.com/25948390/162583157-5549d381-1364-4300-915e-f3563dc471f9.png">

## Running locally

To run the website you need to open two terminal windows and run 

- `hugo serve`
- `yarn tailwind --watch`

This will allow you to work on the website by having a copy running on localhost:1313

Any changes should be immediately reflected.

## Deployment

The site is deployed with CloudFlare Pages, `yarn build` is ran on deploy and everything from the `./public` directory is served.
