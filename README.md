# Ublue website

This page is

## Contributing

This section is about adding/editing images/features/desktops on the page. For development information, checkout the development section.

All of the data for the website lies in the content directory. Inside you'll find two files.

`images.yml` contains all of the main image metadata. Some of this might be able to be queried from an API in the future, but currently the official Github APIs relating to container metadata on Github Container Registry are pretty lacking.
All of the documentation needed to contribute to `images.yml` live in the document itself. If something is not detailed there, either the documentation is a bit behind or the feature is not implemented yet. Go ahead and ask!

`featureDefinitions.ts` contains the definitions and metadata for the features and desktop environments. If there's an important feature that more than one and less than all of the containers have it should probably be added. The desktop environments should be updated to include exactly those desktop environments and window managers that the images showcased on the site use. More documentation for `featureDefinitions.ts` also live in the file itself.

## Development

This website is built using Astro, Svelte, Typescript and TailwindCSS. Some useful commands for this project are declared in the justfile and can be used with the just command runner. This project uses pnpm instead of npm for its superior speed and effiency.

#### Why Typescript and TailwindCSS?

These two are grouped together eventhough they are tools with totally different usecases because the reason for their usage in this project is the same: maintainability. Both provide good conventions for making good code and make it easier to understand the code afterwards.
Additionally: Typescript (by it's very nature) makes it possible to use interface and enums as first-class language features with autocomplete support. This makes it way easier to pass around data in objects.

#### Why Astro?

Astro provides a good foundation for building statically generated (and server rendered) webpages using modern javascript/typescript and popular web component libaries. IMO it is quite fun to work with, and there's rarely any problems with it. This website could've been a Svelte SPA, but with Astro there's always the possibility of expanding this page into a static multi-page website.

#### Why Svelte?

Svelte (IMO) is a breeze to work with. The reactivity is effortless and the syntax on top of standard HTML is pretty minimal and elegant. HAving a JS framework was basically necessary to have a functioning filtering system without making total spaghetti code, so Svelte was the obvious choice.
