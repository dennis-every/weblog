# README

- Works like a charm
- Follow this: https://github.com/rails/docked
- Visit: http://localhost:3000/posts

# Alternatively use a Dockerfile

- Add the Dockerfile to the root path
- Build the image
  - `docker build -t weblog .`
- Run the image in a container with rails server
  - `docker run --rm -it -v ${PWD}:/rails -v ruby-build-cache:/bundle -p 3000:3000 weblog rails server`
- Open rails console in this container
  - `docker exec -it <container_name_or_id> rails console`
