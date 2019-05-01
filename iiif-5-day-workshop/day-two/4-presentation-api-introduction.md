# Presentation API Deep Dive

## Introduction

Hopefully, through the process of slowly building your own image viewer, two things that help explain why something like the IIIF Presentation API exists.

### Image viewers need more than just images.
They need specific kinds of metadata to orchestrate a user's complex interaction with a set of images. Data like the order of the images, the ways individual images should be used, metadata about the object represented by a set of images, metadata about individual images.

### Image viewers are hard to build.
They take time and resources to maintain over time. If everyone had to build a new image viewer for their unique set of images, the world would be full of thousands of different mediocre viewers that are difficult and expensive to maintain.

## Introducing the IIIF Presentation API
The IIIF community recognized precisely this problem, and proposed standardizing the data that any image view would need. Because viewer applications and their data can be separated, image viewers can be re-used for a data set that is structured according to a standard (or set of rules) that the image viewer understands. The IIIF Presentation API is precisely this standard, and a IIIF compliant viewer is an image viewer that understands and knows how to display data that is structured according to these rules.

Today, we're going to look at the "guts" of this standard and learn how to structure our data according to the rules of the IIIF Presentation API.

First, let's look at the conceptual model of the IIIF Presentation API and then we will begin building a manifest together.
