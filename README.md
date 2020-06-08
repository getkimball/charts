# Get Kimball Helm Charts

Helm charts used by/for Kimball applications

## Packaging new charts

```
git checkout [CHART]-[VERSION]
# Update [VERSION] for [CHART in charts/[CHART]/Chart.yaml

helm package [CHART]
mv [CHART]-[VERSION].tgz stable
helm repo index stable --url https://getkimball.github.com/charts
git add -p stable
git commit
git push origin [CHART]-[VERSION]
```
