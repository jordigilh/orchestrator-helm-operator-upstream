# orchestrator-helm-operator

This project was created to evaluate the option of delivering the orchestrator deployment as a helm-based operator.
The repository was created by:

```
mkdir orchestrator-helm-operator
cd orchestrator-helm-operator
operator-sdk init --plugins helm --kind Orchestrator --group parodos.dev --version v1alpha1 --domain parodos.dev --helm-chart=orchestrator --helm-chart-repo=https://parodos-dev.github.io/orchestrator-helm-chart --helm-chart-version=0.1.21 --project-name orchestrator
```

To test the operator locally, with `devmode` orchestrator deployment:
```
make install run
oc apply -f config/samples/parodos.dev_v1alpha1_orchestrator-devmode.yaml
```
