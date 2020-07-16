# Get Kimball Helm Charts

Helm charts used by/for Kimball applications

## Add this repository

```
helm repo add getkimball https://getkimball.github.io/charts/stable
```

## Packaging new charts

```
git checkout -b [CHART]-[VERSION]

# Update [VERSION] for [CHART in charts/[CHART]/Chart.yaml
# Make your changes
# Git stage your changes

helm package charts/[CHART]
mv *.tgz stable
helm repo index stable --url https://getkimball.github.io/charts/stable
git add -p stable
git add stable/*.tgz
git commit
git push origin [CHART]-[VERSION]
```
