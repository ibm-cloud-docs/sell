---

copyright:
  years: 2022, 2023
lastupdated: "2023-01-06"

keywords: troubleshoot software, HTTPS protocol, repo, github, tgz

subcollection: sell

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I upload my product's source details from my GitHub repository?
{: #repo-upload-error}
{: troubleshoot}

If you encounter an error when you are importing your software into a private catalog, a file might be missing or formatted incorrectly within your source repository. Or, if your repository is private, authentication failed.
{: shortdesc}

You receive the following error message when you try to upload your product's source details from a GitHub repository to your private catalog:
{: tsSymptoms}

> There was an error while contacting this URL.

This error typically occurs because a file is missing or formatted incorrectly. Or, if your repository is private, there was an error authenticating with it.
{: tsCauses}

Do one of the following, depending on your product's delivery method:
{: tsResolve}

- If you are uploading a `.tgz` or `.yaml` file, make sure that the file is formatted correctly. For a `.yaml` file, all required fields must be specified in the file. A `.tgz` file must contain a single `root` folder with all source files contained within that folder.
- If your source details are in a private repository, make sure that you have a personal access token or secret to authenticate. For more information, see [Importing a version to your private catalog](/docs/sell?topic=sell-sw-validate&interface=ui#sw-validate-add).
- Make sure that your repository supports HTTPS protocol.

For more information, see [Managing releases in a repository](https://docs.github.com/en/free-pro-team@latest/github/administering-a-repository/managing-releases-in-a-repository){: external}.
