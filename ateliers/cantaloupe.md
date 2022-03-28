# Cantaloupe

current v.5.0.5

requires: java 11+

[Doc](https://cantaloupe-project.github.io/manual/5.0/getting-started.html)

[IIIF github](https://github.com/IIIF/awesome-iiif)

Based on [IIIF training](https://training.iiif.io/intro-to-iiif/), but with updated cantaloupe version 

## Running Cantaloupe

from the folder where it is installed (lmk/opt/cantaloupe)


```bash
java -Dcantaloupe.config=/cantaloupe.properties -Xmx2g -jar cantaloupe-5.0.x.jar
```

Images are in `/home/lmk/Documents/ouvroir/imagesIIIF/`

```bash
FilesystemSource.BasicLookupStrategy.path_prefix = /home/lmk/Documents/ouvroir/imagesIIIF/
```



Assuming you have an image named IMG_7106.JPG, try accessing:

- http://localhost:8182/iiif/3/IMG_7106.JPG/info.json
- http://localhost:8182/iiif/3/IMG_7106.JPG/0,0,1200,1200/max/0/default.jpg

### Endpoint control panel

In `cantaloupe.properties`, set `endpoint.admin.enabled` to true and define username and password

- http://127.0.0.1:8182/admin