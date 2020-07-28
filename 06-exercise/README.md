# Exercise

If there are any questions, ask us anytime.

## Production grade deployment

1. Make sure you switched your context (check that `kubectl config get-contexts` shows your personal namespace in the `NAMESPACE` column)
2. Deploy the [production grade deployment](../03-production-grade-deployments) to your namespace

## Dockerizing the exercise app

If you don’t have docker installed, you can use `syseleven/exercise-app:1.0.0` which we pushed to [hub.docker.com](https://hub.docker.com/repository/docker/syseleven/exercise-app) for you.

1. Create a Dockerfile
2. Build the docker image
3. Test it locally
4. Push it to Docker Hub or another registry

## Deploy the exercise app

1. Create a Deployment
2. Create a Service of type ClusterIP (no external LoadBalancer)
3. Create a ConfigMap with a USERNAME and inject it into the Deployment as an environment variable

## Improving the exercise app

1. Add a HorizontalPodAutoscaler to the exercise app
2. Perform a load test against your application, e.g. with Apache Bench: `ab -c 100 -n 1000 http://<IP_ADDRESS>/`. If you don’t have a tool for that, ping the tutors who will generate some load for you.
3. Check that your autoscaling works when there is load generated
4. Adjust the pod resources according to the actual usage when they are under load
5. Look into the logs to see that the web server responds correctly to the incoming requests

If you arrived here, please let us know.

## Bonus

* Make the repository in the Docker registry private, see https://kubernetes.io/docs/tasks/configure-pod-container/pull-image-private-registry/
