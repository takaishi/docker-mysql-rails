# README

## Install

```shell
brew install docker docker-compose docker-machine
docker-machine create --driver virtualbox default
eval $(docker-machine env default)
docker-machine start default
cd ${RAILS_ROOT}
docker-compose build
docker-compose run web rake db:create
docker-compose run web rake db:migrate
docker-compose up
open http://$(docker-machine ip default):3000
```

Please feel free to use a different markup language if you do not plan to run
<tt>rake doc:app</tt>.
