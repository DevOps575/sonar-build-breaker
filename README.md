![.github/workflows/main.yaml](https://github.com/DevOps575/sonar-build-breaker/workflows/.github/workflows/main.yaml/badge.svg) [![Quality gate](https://sonarcloud.io/api/project_badges/quality_gate?project=sonar_test_github_project)](https://sonarcloud.io/dashboard?id=sonar_test_github_project) [![Known Vulnerabilities](https://snyk.io/test/github/jkumar19/sonar-build-breaker/badge.svg?targetFile=Dockerfile)]
# Validating Sonar Analysis and Quality Gates

This GitHub action is used to fail GitHub workflow in case Quality Gates failed. This GitHub action expect the following required parametes:

| Parameters   | Required | 
|--------------|----------|
| sonar_url    |   yes    |
| sonar_token  |   yes    |
| project_key  |   yes    |
| sonar_branch |   yes    |

Sample Code Example:

```
- name: Sonar Build Breaker
  uses: jkumar19/sonar-build-breaker@v1.0.0
  with:
    sonar_url: "https://sonarcloud.io"
    sonar_branch: "main"
    sonar_token: ${{ secrets.SONAR_TOKEN }}
    project_key: "sonar_project_key"
```
