stages:
  - build
  - test
  - deploy

build:
  stage: build
  image: node:latest
  script:
    - npm install
    - npm run build

test:
  stage: test
  image: node:latest
  script:
    - npm install
    - npm run test

deploy:
  stage: deploy
  image: node:latest
  script:
    - echo "Deploying the app..."
