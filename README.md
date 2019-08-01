# Circleci-101
version: 2
jobs:
  build:
    docker:
    - image: debian:stretch
    steps:
    - checkout
    - run:
        name: Greeting
        command: echo Hello, world.
    - run:
        name: Print the Current Time
        command: date
workflows:
  version: 2
  workflow:
    jobs:
    - build
