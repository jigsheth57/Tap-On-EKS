# Tap-On-EKS
This document provides an instructions for MacOS on installing Tanzu Application Platform on EKS.

## Review the prerequisties
1. Install following CLIs
  - AWS ([brew install awscli](https://formulae.brew.sh/formula/awscli))
  - Kubectl ([brew install kubernetes-cli](https://formulae.brew.sh/formula/kubernetes-cli#default))
  - Kubectx ([brew install kubectx](https://formulae.brew.sh/formula/kubectx#default))
  - Knative ([brew install kn](https://formulae.brew.sh/formula/kn#default))
  - Jq ([brew install jq](https://formulae.brew.sh/formula/jq#default))
  - Jupyterlab ([brew install jupyterlab](https://formulae.brew.sh/formula/jupyterlab#default)) (Here's the [detail instructions](https://medium.com/@iamclement/how-to-install-jupyter-notebook-on-mac-using-homebrew-528c39fd530f))
  - Pivnet ([brew install pivotal/tap/pivnet-cli](https://github.com/pivotal-cf/pivnet-cli))
  - Carvel Tooling ([brew tap vmware-tanzu/carvel && brew install ytt kbld kapp kwt imgpkg vendir](https://github.com/vmware-tanzu/homebrew-carvel))
  - Helm ([brew install helm](https://formulae.brew.sh/formula/helm))

2. Configure `aws` cli to [work with your credentials](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html).
3. Retrieve/create **UAA API TOKEN** on [TanzuNet](https://network.pivotal.io/) under __Edit Profile__ and __REQUEST NEW REFRESH TOKEN__ and configure your system environment with `export API_TOKEN=YourToken`
4. Install Bosh kernal for Jupyterlab.
`pip install bash_kernel && python -m bash_kernel.install`

## Standup EKS Cluster
- Start `jupyter lab` and open `CreateEKSCluster` notebook.

## Standup Secure Harbor Registry
- Start `jupyter lab` and open `StandupHarbor` notebook.
