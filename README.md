Portable Discography Schema
================

There are many existing schemas for music metadata on the web [1]. However, existing music schemas tend to be either too specific to their implementation, too general for discography use, or too difficult to implement. 

The goal of this project is to define a discography schema in YAML/JSON to allow a band, artist, or record label to manage their discography metadata using a portable and human readable file format. It is not intended to replace fully spec'd XML schemas, or backend databases, it is meant to complement and help connect existing applications and services.

Example use cases for a YAML/JSON format:
  - Import/export discography information into open web apps like Pushtape [2] and Cash Music
  - A resource for generating flat file music sites, using Jekyll, Express JS, or similar
  - An API response for a music website
  - Input for a streaming music player on the web
  - Networked music discography applications (i.e. a decentralized, open source version of Spotify)
  - Can be read and edited by hand, as well as by a machine
  - Can be converted quickly into many other formats

# Caveats
  - This is an *experimental* YAML implementation for importing/exporting discographies.
  - How this information is parsed and displayed is dependent on the application that imports/exports it.

# Structure
- CHANNEL INFO: The first level items describe the discography itself, similar to RSS channel level info. Title, Publish date, URL, Image, Author, Description.

- RELEASES is an array of items. Each item can either be a single track entity or an album entity containing an array of tracks. Your discography should be structured in such a way that you only have to define things once, and that nesting and track order are implied. We want to avoid overengineered semantics, data redundancy and circuitious node referencing when possible to keep things human readable.

# Todos
  - Check YAML formatting / compliance. Minimize indenting?
  - Provide example in JSON
  - Clarify what minimum fields are required to make this useful: i.e. Every release needs a Title & URI

# References
[1] Existing Music Schemas for the web
  - Musicbrainz XML
  - Microformat
  - Discogs JSON
  - Music Ontology
  - XSPF XML
  - Podcasts / RSS
  - Media RSS
[2] Background: http://drupal.org/node/1226226

