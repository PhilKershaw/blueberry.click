# README

## Deployment
- Build new image `docker build -t philkershaw/phil.kershaw.ooo:[new tag] .`
- Push to registry `docker push philkershaw/phil.kershaw.ooo:[new tag]`
- Go to `https://hub.docker.com/r/philkershaw/phil.kershaw.ooo/~/settings/` and make repo temporarily `public` until deployed
- First deployment:
-- `kubectl run --image=philkershaw/blueberry.click blueberry-click`
-- `kubectl expose deployments/blueberry-click --type=NodePort --port=80`
-- ``
- Subsequent deployments:
-- Deploy new image `kubectl set image deployment/phil-kershaw-ooo phil-kershaw-ooo=philkershaw/phil.kershaw.ooo:[new tag]`
- Go to `https://hub.docker.com/r/philkershaw/phil.kershaw.ooo/~/settings/` and make repo `private`