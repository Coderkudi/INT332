a read only blueprint

contains:

- base os(minimal)
- application code
- libraries and dependencies
- runtime
- configuration

example:

- python:3.11-slim is the image
  this image already includes:

* linux os
* python 3.11
* standard python libraries

# image layers

---

###########****\*\*\*\*****\*\*\*\*****\*\*\*\*****############333

# Container Images

## Definition

A container image is a read-only template used to create containers.
It contains everything required to run an application, including the application code, system libraries, dependencies, and runtime environment.

---

## Image vs Container

| Image                 | Container                    |
| --------------------- | ---------------------------- |
| Blueprint or template | Running instance of an image |
| Read-only             | Writable environment         |
| Stored on disk        | Running process              |

Example:

docker run nginx

This command creates a container from the nginx image and starts it.

---

## Components of a Container Image

A container image typically includes:

- Base operating system
- Runtime environment
- Application dependencies
- Application code
- Configuration files

---

## Image Layers

Container images are built using multiple layers.

Each layer represents a change in the filesystem.

Example layers:

Layer 1 → Base operating system
Layer 2 → Install programming language runtime
Layer 3 → Install dependencies
Layer 4 → Add application code

These layers are stacked together to form the final container image.

---

## Benefits of Image Layers

- Faster builds because unchanged layers are reused
- Efficient storage because multiple images can share layers
- Easier updates when only a specific layer changes

---

## Image Storage

Images are stored locally on the system after being pulled from a registry.

Command to view images:

docker images

Each image has a repository name, tag, and unique image ID.

---

## Read-Only Images

Container images are read-only.

When a container is created, Docker adds a writable layer on top of the image layers.

This writable layer stores runtime changes made by the container.

---

## Conclusion

Container images provide a portable and consistent way to package applications and their dependencies.
They form the foundation for creating and running containers.
