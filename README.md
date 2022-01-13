# Lingq.com API

This is unofficial Lingq.com OpenAPI specification.

Luckily, http://lingq.com provides a RESTful API and so potentially any developer can use it. 
Unfortunately, at the time of writing, they don't provide either relevant documentation or formal specification.

This project is an enthusiastic attempt to fill this gap.

## What is included

This spec is not comprehensive and doesn't pretend to be. You're free to add the missing parts.

Here is  list of methods and models covered by the spec:

### Methods

- `/{lang}/collections/{id}` - fetch course by id
- `/{lang}/lessons/{id}` - fetch lesson by id
- `/{lang}/cards` - fetch user cards (todo)
- `/{lang}/lessons/{id}/sentences` - fetch lesson text sentences (todo)

### Models

- Collection (i.e. Course)
- Lesson
- Bookmark
- Card
- Word
- TokenizedTextGroup
- Token

In the near future I'm going to contact Lingq.com developers, requesting to evaluate this spec coverage degree.

## Prehistory

It began recently with a script for fetching lessons and their audio. 

Soon I discovered that it's difficult to proceed without some formal API definition. So I created a 
set of defs in OpenAPI format, beginning with a few API methods I personally needed.

When more requests and schemas followed, I found it reasonable to extract the spec into a separate project to 
let others use it.

## Why NPM packaging?

Because some package manager was required, and I picked one that I liked. 

You see, I can't bear the default OpenAPI format, as it's flawed: it doesn't support YAML references and anchors.
And without them, I don't find writing API spec entertaining at all. So I do write it in normal YAML and then convert it 
to JSON, which OpenAPI Generator understands as well. Checkout `package.json`'s `scripts` section for more details. 

## Contribution

It's welcome.
