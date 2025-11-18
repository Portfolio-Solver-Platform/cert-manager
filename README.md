# cert-manager

Certificate management for the platform using cert-manager.

## First Time Setup

Run `bootstrap.sh` to add the Helm repository.

## Usage

Run `skaffold dev` to deploy cert-manager in development mode.
For production, use `skaffold run -p prod`.

## Verification

Check that cert-manager is running:
```bash
kubectl get pods -n cert-manager
kubectl get crds | grep cert-manager
```

You should see three pods running:
- cert-manager
- cert-manager-webhook
- cert-manager-cainjector

## Contributing

cert-manager is deployed via Helm chart dependency. To update the version, modify `helm/Chart.yaml`.
