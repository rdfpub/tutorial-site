# The rdfpub Tutorial Site

This is the source for the rdfpub tutorial site, a living example of an rdfpub
site that documents and demonstrates all the facets of an rdfpub site. Browsing
[the live tutorial site](https://rdf.pub/tutorial) is the easiest way to
reference the tutorial, but you can also run the tutorial site on your local
machine.

## How to run this site

The easiest way to run this site is to run a pre-built Docker image of the
site like so (for which you will need [Docker](https://www.docker.com)):

```bash
docker run -p 80:8081 ghcr.io/rdfpub/tutorial-site
```

If the image runs successfully, then you should be able to visit the tutorial
site in your browser at <http://localhost/tutorial>.

If you're looking to get more hands-on with rdfpub, you can download the
tutorial site's code and build it yourself like so:

```bash
# Clone the tutorial site repo
git clone https://github.com/rdfpub/tutorial-site

# Generate a Docker image of the tutorial site
docker run                                     \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v `pwd`/tutorial-site:/rdfpub/input:ro      \
  ghcr.io/rdfpub/generator:2.3.0               \
  -t rdfpub/tutorial-site

# Run the tutorial site
docker run -p 80:8081 rdfpub/tutorial-site
```

