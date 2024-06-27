---


copyright:
  years: 2020, 2024

lastupdated: "2024-06-26"

keywords: software, third-party software, sellers, partners, validate, test, partner center

subcollection: sell

---

{{site.data.keyword.attribute-definition-list}}

# Onboarding software to your private catalog
{: #sw-validate}

The process to onboard your software includes importing a version to your private catalog, configuring the deployment details, setting any license requirements, and validating that the version can be successfully installed on the target infrastructure that you require.
{: shortdesc}

## Before you begin
{: #sw-validate-prereqs}

1. Upload your source code to a release in your GitHub, GitLab, or Azure repository. For more information, see [Setting up your source code repository](/docs/sell?topic=sell-source-repo-setup).
1. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more information.
1. Make sure you're assigned the editor role on the catalog management service. See [Assigning access to account management services](/docs/account?topic=account-account-services).
1. Set up the test environment that was previously created for you:

    * Install the {{site.data.keyword.cloud_notm}} CLI and the {{site.data.keyword.cloud_notm}} Schematics plug-in. See [Setting up the CLI](/docs/schematics?topic=schematics-setup-cli).

    * Upload a readme file that contains your product installation instructions to your source repository. See [Setting up your source code repository](/docs/sell?topic=sell-source-repo-setup).
    * For containerized apps:
        * Create your [Kubernetes cluster](/docs/containers?topic=containers-getting-started) or [Red Hat OpenShift cluster](/docs/openshift?topic=openshift-getting-started).
        * For deployments to {{site.data.keyword.cloud_notm}} Kubernetes Service, [set up your Helm chart](/docs/containers?topic=containers-helm).
        * For deployments to Red Hat OpenShift, set up your [Helm chart](/docs/openshift?topic=openshift-helm) or [Operator](/docs/openshift?topic=openshift-operators).
    * For virtual server images:
        * Review the list of [supported images](/docs/vpc?topic=vpc-about-images).
        * If required, create your [Terraform template](/docs/schematics?topic=schematics-getting-started). Virtual server images for VPC do not require a Terraform template.
        * Create an instance of [{{site.data.keyword.cloud_notm}} Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage) and add your image to a bucket.

## Importing a version to your private catalog
{: #sw-validate-add}
{: ui}

Complete the following steps to import a version of your software to your private catalog. Your private catalog was created for you as part of [Getting set up to sell software](/docs/sell?topic=sell-sw-getting-started).

1. In the {{site.data.keyword.cloud_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Partner Center** > **My products**.
1. Select the product that you're onboarding.
1. From the Software tab, click **Import a version**.
1. Select your deployment method.
1. Select whether you are adding your product from a private or public repository. For Operators, select your source repository and then choose private or public repository.
1. Enter your source URL.

    You can review the following list of supported formats per software type:

    * Helm chart: `https://raw.githubusercontent.com/IBM/charts/master/repo/ibm-helm`
    * Node-RED Operator: `https://github.com/IBM-Cloud/operator-bundle-sample/archive/refs/tags/v0.0.3.tar.gz`
    * Operator bundle from a {{site.data.keyword.openshiftshort}} registry: For an example, select the `Akka Cluster Operator` from the list of available Operators in the Certified repository.
    * OVA image: `https://github.com/gcatalog/OVA-sample/blob/main/ova-sample.yaml`
    * Terraform template: `https://github.com/IBM-Cloud/terraform-sample/archive/refs/tags/v1.1.0.tar.gz`
    * Virtual server image with Terraform: `https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/releases/download/v1.0/isv-vsi-product-deploy-sample.tar.gz`
    * Virtual server image for VPC: Select an image from the list of available images that were imported into your VPC, or import a new image to your account.

    A virtual server image for VPC can only be added to one product within one private catalog at a time. If the virtual server image you want to import is already imported into another product, you must remove the image from that product or delete the product before you add the virtual server image to a new product.
    {: note}

    If you're adding your product from a private repository, you can choose to provide a personal access token or you can use a secret. Instead of giving users a personal access token, you can give them access to a secret, add the token to a secret, and centrally manage all tokens and access the secret allows.

    * If you're using a personal access token, select **No** to indicate that you aren't using a secret and provide your personal access token.
    * If you're using a secret, select **Yes** and click **Select from Secrets Manager**. Select your service instance, secret group, and secret. If you don't see your secret, make sure you're using the correct secret group and service instance.

    The message `No service instance available` might be displayed if you haven't created a secret or if you don't have the correct access to use secrets, even if you have service instances that are created.
    {: note}

1. If applicable, set your deployment target and add your software version.
1. Click **Add version**.

## Configuring the version details
{: #sw-validate-cfg-deploy}
{: ui}

1. From the version list, click the row that contains your software.
1. Review the version details, and click **Next**.
1. Depending on your software type, there might be additional steps, including setting deployment values.
1. Click **Next**.

### Set deployment values
{: #sw-set-values}
{: ui}

If applicable to your software type, you can set deployment values that users are required to specify when they install the software. You can add new deployment values or import deployment values from an existing version.

#### Add new deployment values
{: #sw-add-values}
{: ui}

1. Click **Configure version** > **Next**.
1. Click **Add deployment values**.
1. In the table, select **Parameter** > **Add** to select and add all options.
1. If necessary, you can customize the parameters by selecting them from the table and clicking **Edit**.

#### Import existing values
{: #sw-import-values}
{: ui}

Complete these steps if you previously set deployment values for an existing version and want to import the values to your current version.

Imported values don't replace any deployment values that you already added to your current version.
{: important}

1. Click **Configure version** > **Next**.
1. Click **Add deployment values**.
1. Click **Import values from a previous version**
1. Select the version that contains the values that you want to import.
1. Click **Import**.
1. If necessary, you can customize the parameters by selecting them from the table and clicking **Edit**.

### Edit output value descriptions
{: #sw-output-values}

{{site.data.content.description-output-values}}

{{site.data.content.note-output-values}}

{{site.data.content.steps-desc-output-values}}

{{site.data.content.steps-output-value}}

### Define IAM access
{: #sw-define-IAM-access}

If applicable to your software type, you can add the service access and platform access roles that are required to install your product from the {{site.data.keyword.cloud_notm}} catalog. You can define new IAM access or import IAM access that you set in an earlier version.

#### Defining new IAM access
{: #sw-new-access}

{{site.data.content.steps-define-desc-iam-access}}

{{site.data.content.steps-define-IAM-access}}

#### Importing existing IAM access
{: #sw-import-access}

Complete the following steps if you previously defined IAM access for an existing version and want to import the values to your current version.

Imported IAM access doesn't replace any IAM access that you already added to your current version.
{: note}

1. Click **Configure version** > **Next** > **Next**.
1. Click **Add**.
1. Click **Import IAM access from a previous version**.
1. Select the version that contains the IAM access that you want to import.
1. Click **Add**.

## Adding license agreements
{: #sw-validate-add-license}
{: ui}

If users are required to accept any license agreements beyond the {{site.data.keyword.cloud_notm}} Services Agreement when they install the software, provide the URL to each agreement or import licenses from an existing version.

### Add new license agreements
{: #sw-add-new-license}
{: ui}

1. Click **Add license agreements** > **Add license**.
1. Enter the name and URL, and click **Add license**.
1. After entering all additional license agreements, click **Next**.

### Import license agreements
{: #sw-import-license}
{: ui}

Complete these steps if you previously added license agreements for an existing version and want to import the licenses to your current version.

Imported licenses don't replace any license agreements that you already added to your current version.
{: important}

1. Click **Add license agreements** > **Add license**.
1. Click **Import licenses from a previous version**.
1. Select the version that contains the licenses that you want to import.
1. Click **Import**.

## Reviewing your readme file
{: #sw-validate-readme-review}
{: ui}

When users install the software, they can view product information by clicking the Readme link. The information in the Readme link is generated from the readme file that you uploaded to your source repository.

1. From the Edit readme tab, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
1. Preview how the information in the readme file will be displayed to users when they are installing the software.
1. To make updates, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit") next to the Readme section title.
1. Click **Save**.
1. Click **Next**.

If you are importing a virtual server image for VPC, the readme file is not automatically generated. Copy and paste the contents of the [readme file template](/media/docs/downloads/software/sw-readme-tab-template.md){: external} and make updates as needed.
{: note}

## Validating the product
{: #sw-validate-validate-product}
{: ui}

The steps to validate your product can vary based on the type of software that you're onboarding.

1. From the Validate product tab, configure your validation target, and click **Next**. This step applies only to Helm charts and Operators.
1. Configure your workspace, and click **Next**. This step applies only to Helm charts, Operators, Terraform templates, and virtual server images with Terraform.
1. Click **Validate**.

To monitor the progress of the validation process, click **View logs**.
{: tip}

## Validating your software by using the API
{: #sw-validate-edits-api}
{: api}

You can validate your software by calling the [Catalog Management API](/apidocs/resource-catalog/private-catalog?code=java#validate-install){: external}.

```java
String authRefreshToken = "{authRefreshToken}";
String versionLocator = "{versionLocator}";
ValidationInstallOptions installOptions = new ValidationInstallOptions.Builder().xAuthRefreshToken(authRefreshToken).versionLocId(versionLocator).build();
Response<Void> response = service.validationInstall(installOptions).execute();
System.out.println(response.getResult());
```
{: codeblock}
{: java}

```javascript
versionLocator = "{versionLocator}";
authRefreshToken = "{authRefreshToken}";
response = await service.validationInstall({ 'versionLocatorId': versionLocator, 'xAuthRefreshToken': authRefreshToken });
console.log(response);
```
{: codeblock}
{: javascript}

```python
authRefreshToken="{authRefreshToken}"
versionLocator = "{versionLocator}"
response = self.service.validation_install(version_locator_id=versionLocator, x_auth_refresh_token=authRefreshToken)
print(response)
```
{: codeblock}
{: python}

```go
versionLocator := "{versionLocator}"
authRefreshToken := "{authRefreshToken}"
installOptions := service.NewValidationInstallOptions(versionLocator, authRefreshToken)
response, _ := service.ValidationInstall(installOptions)
fmt.Println(response)
```
{: codeblock}
{: go}

## Manage security and compliance controls
{: #sell-controls}
{: ui}

Controls are safeguards that are used to meet security and compliance requirements. Only controls that are supported by Security and Compliance Center, formatted correctly, and validated by Code Risk Analysis and Security and Compliance Center scans appear in the catalog. For more information, see [Formatting controls in your readme file](/docs/sell?topic=sell-sell-format-controls).

1. Click **Add controls**.
1. Choose a profile.
1. Select the controls that you want to add to your version.
1. Click **Add**.
1. In the Code Risk Analyzer scan section, click **Run scan**.
1. Wait for the scan to finish.
1. In the Security and Compliance Center scan section, select the profile that you scanned.
1. Select the Security and Compliance Center scan.
1. Click **Add scan**.
1. Click **Next**.

## Review requirements
{: #catalog-manage-review-reqs}

You must complete validation and any other requirements to publish your product.
