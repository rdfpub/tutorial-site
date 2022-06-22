# The rdfpub Tutorial Site

This is the tutorial site for rdfpub, a static-ish site generator for
publishing rich [RDF](https://www.w3.org/TR/rdf11-primer/) data to the World
Wide Web. The links at the top of the page can be followed to learn about the
various facets of an rdfpub site, including instructions and examples for how
to create your own rdfpub site.

## Source

The [rdfpub source code](https://github.com/rdfpub/generator) is maintained
at GitHub along with other supporting projects within
[the rdfpub organization](https://github.com/rdfpub), including
[the source code for this tutorial site](https://github.com/rdfpub/tutorial-site).

## How to run this site

The easiest way to run this site is to run a pre-built Docker image of the
site like so (for which you will need [Docker](https://www.docker.com)):

```bash
docker run -p 80:80 ghcr.io/rdfpub/tutorial-site
```

If you're looking to get hands-on with rdfpub, there are alternate instructions
for how to run this site from source in the
[build/run/deploy lesson](/lessons/build-run-deploy).

## Thanks!

A big thanks to all of the developers of the projects that rdfpub depends
on, including but not limited to those who helped develop
[RDF4J](https://www.rdf4j.org"), [Handlebars](https://handlebarsjs.com),
[OpenResty](https://openresty.org),
[markdown-it](https://github.com/markdown-it/markdown-it), and
[SimpleCSS](https://www.simplecss.org). Projects like rdfpub
couldn't exist without the bedrock of technologies that all of you have
contributed to.

And a thanks to you, the person reading this, for taking the time to check
out this nifty little passion project. 🙂
