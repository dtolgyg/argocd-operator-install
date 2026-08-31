# argocd-operator-install

IMG="quay.io/argoprojlabs/argocd-operator:v0.18.0"
cd config/manager && kustomize edit set image controller=${IMG}
cd ../..
kustomize build config/default >> full.yaml