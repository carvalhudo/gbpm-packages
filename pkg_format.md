GBP format
==========

### Introduction

This document aims to describe the ```.gbp``` (git-based package) file format, used by gbpm.

### Package format

**Header**

```
 0               1               2               3
 0 1 2 3 4 5 6 7 0 1 2 3 4 5 6 7 0 1 2 3 4 5 6 7 0 1 2 3 4 5 6 7
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|     version   |                     mbz                       |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
```

- version: Version of the package format, composed by a major version (high nibble) and a minor version (low nibble).
- mbz: Padding bytes.

**Section**

The ```gbp``` format contains 3 data sections, where 2 of them are mandatory. The mandatory sections aThe section has the following format:

```
 0               1               2               3
 0 1 2 3 4 5 6 7 0 1 2 3 4 5 6 7 0 1 2 3 4 5 6 7 0 1 2 3 4 5 6 7
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|     sec_id    |                   sec_len                     |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
|                               ...                             |
|                            sec_data                           |
|                               ...                             |
+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+-+
```

- sec_id: ID of the section. It can be 0 for scripts section (mandatory), 1 for package section (mandatory) or 2 for config section (optional). The sections will be described further in this document.
- sec_len: Length of the section.
- sec_data: Payload of the section.

### Package sections

#### Scripts

jaosidj

#### Package

asdjoasidjoasidj

#### Config

asidjoasidjaosi
