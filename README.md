# Docker Jelastic Actions

This action allows you to deploy your docker image to Jelastic PaaS.

## Inputs
- `dockerhub_username` - **Required**. DockerHub username
- `dockerhub_password` - **Required**. DockerHub password or access token
- `dockerhub_repo` - **Required**. DockerHub repository name (e.g. myrepo/myimage)
- `image_tag` - **Required**. Docker image tag (e.g. latest, 1.0.0, etc.)
- `jelastic_url` - **Required**. Jelastic API URL
- `jelastic_env` - **Required**. Jelastic environment name
- `nodegroup` - **Required**. Jelastic node group name (e.g. cp, vds, etc.)
- `redeploy_token` - **Required**. Jelastic redeploy token

## Example usage
```yaml
- uses: jelastic/jelastic-action@v1
  with:
    dockerhub_username: ${{ secrets.DOCKERHUB_USERNAME }}
    dockerhub_password: ${{ secrets.DOCKERHUB_PASSWORD }}
    dockerhub_repo: myrepo/myimage
    image_tag: latest
    jelastic_url: https://app.j.layershift.co.uk/1.0/
    jelastic_env: myenv
    nodegroup: cp
    redeploy_token: ${{ secrets.REDEPLOY_TOKEN }}
```
