version: 2.1

jobs:
  build_and_test:
    docker:
      - image: cimg/node:current
    steps:
      - checkout
      - run: npm install
      - run: npm test

workflows:
  build_and_test:
    jobs:
      - build_and_test 
