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
docker run -p 80:8081 ghcr.io/rdfpub/tutorial-site
```

If the image runs successfully, then you should be able to visit the tutorial
site in your browser at <http://localhost/>.

If you're looking to get more hands-on with rdfpub, you can download the
tutorial site's code and build it yourself like so:

```bash
# Clone the tutorial site repo
git clone https://github.com/rdfpub/tutorial-site

# Generate a Docker image of the tutorial site
docker run                                     \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v `pwd`/tutorial-site:/rdfpub/input:ro      \
  ghcr.io/rdfpub/generator:2.1.0               \
  -t rdfpub/tutorial-site

# Run the tutorial site
docker run -p 80:8081 rdfpub/tutorial-site
```

## Thanks!

A big thanks to all of the developers of the projects that rdfpub depends
on, including but not limited to those who helped develop
[RDF4J](https://rdf4j.org), [Handlebars](https://handlebarsjs.com),
[OpenResty](https://openresty.org),
[markdown-it](https://github.com/markdown-it/markdown-it), and
[SimpleCSS](https://www.simplecss.org). Projects like rdfpub
couldn't exist without the bedrock of technologies that all of you have
contributed to.

And a thanks to you, the person reading this, for taking the time to check
out this nifty little passion project. 🙂
