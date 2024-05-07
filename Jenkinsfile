stages:
  - build
  - deploy
build:
  stage: build
  script:
    - npm install
    - npm run build
    - cp config.$ENV.json dist/config.json
  artifacts:
  paths:
    - dist/
deploy:
  stage: deploy
  script:
    - deploy-script.sh $ENV
  environment:
    name: $ENV
    url: http://example.com
  only:
    - master