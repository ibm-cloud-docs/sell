---


copyright:
  years: 2022, 2025
lastupdated: "2025-02-21"

keywords: software, readme, installation, Git, GitHub, repo, repository

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Setting up your source code repository
{: #source-repo-setup}

Set up your source code repository with the artifacts that are required to onboard your software. In addition to source code, your repository contains a readme file that's displayed when you publish your product.
{: shortdesc}

## Creating a release
{: #create-release}

Create a release or tag in your source code repository to deliver and manage versions of your software.
- For GitHub repositories, see [Managing releases in a repository](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository){: external}.
- For GitLab repositories, see [Releases](https://docs.gitlab.com/user/project/releases/#:~:text=In%20GitLab,%20a%20release%20enables,point%20in%20the%20source%20code.){: external}.
- For Azure repositories, see [Use Git tags](https://learn.microsoft.com/en-us/azure/devops/repos/git/git-tags?view=azure-devops&tabs=browser){: external}.

## Uploading your readme file
{: #upload-readme}

Upload a readme file that focuses on helping users to get up and running with your software. When you publish the software, the details of your readme file are available from your product's details page in the {{site.data.keyword.cloud}} catalog.

1. Use the [readme file template](https://cloud.ibm.com/media/docs/downloads/software/sw-readme-tab-template.md){: external} to document the step-by-step instructions for installing your software. If your readme file is missing sections in the template, it will not be approved.
2. Save your updates and name your file `readme.md`.
3. Go to your repository and upload the `readme.md` file.
