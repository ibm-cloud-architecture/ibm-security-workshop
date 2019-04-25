# IKS Security Lab

## Container Registry

IBM Cloud Container Registry helps you to store your docker images. These images can be either accessible by the public using public registry or the access can be restricted to certain users using private registry. Also, this registry allows only the IBM Cloud account users to access the images.

- Multi-tenant
- Highly available
- Scalable

1. Login to your IBM Cloud Account and access the kubernetes clusters in your lab account.

![AccessKubernetes](AccessKubernetes.png)

2. Access the **Demo cluster** under the Kubernetes Clusters.

![AccessCluster](AccessCluster.png)

3. If you click on the **Access** tab, it will give you the instructions to access the cluster in your command line. You can give it try if you are interested.

![IKSCluster](IKSCluster.png)

4. Scroll down to the bottom and you will find an option **creating a registry!** which takes you to the IBM Container Registry. If there is an existing registry, it takes you there or else it will create one for you.

![AccessRegistry](AccessRegistry.png)

5. The **Quick Start** will give you instructions on how you can push your images to the registry.

![PushImages](PushImages.png)

We already pushed some of the images from our demo application.

6. If you click on the **Namespaces**, you can see the existing namespaces in our registry.

![namespaces](namespaces.png)

7. Let us now access **Repositories** and see what are existing in our registry.

![repositories](repositories.png)

8. You can also see all the available images by clicking on **Images**.

![DockerImages](DockerImages.png)

## Vulnerability Advisor

Vulnerability Advisor scans the security status of the docker images that are pushed to the registry namespace. When the image is added to the namespace, it will be scanned automatically by the vulnerability advisor to detect the security issues and potential vulnerabilities.

It will generate a report suggesting the fixes. You can also add exemptions based on your requirements. Fixing the issues that are reported can help you to secure your IBM Cloud infrastructure.

1. If you click on the **Images**, you can see `Security Status` associated with each image.

![SecurityStatus](SecurityStatus.png)

2. Let us now click on one of the issues and see what it shows us. For instance, click on the security issue for location service.

![SecurityIssue](SecurityIssue.png)

3. You can now see various issues of the image here.

![IssuesLocationImage](IssuesLocationImage.png)

4. Click on any of the issues to expand. You can see the reason for your issue and it also suggests you a fix.

![IssueFix](IssueFix.png)

5. If you know your issue can be an exemption, you can create one.

![createExemption](createExemption.png)

6. You can then create a policy exemption and save it.

![createPolicy](createPolicy.png)

7. The issue will be exempted and you can see it.

![policystatus](policystatus.png)

8. Alternatively, you can also access vulnerability advisor and create exemption policies there as well.

You can go to your Kubernetes cluster and access **vulnerability advisor** similar to the Registry.

![AccessVA](AccessVA.png)

9. Click on the **Policy Settings** under Vulnerability Advisor and you can create an exemption for your issue using **Create Exemption**.

![PolicySettingsVA](PolicySettingsVA.png)

10. Find the `Issue ID` for your issue and add it in the **Issue ID** field. Then **Save** the policy.

Here, let us get the issue id of the vulnerability for the location service which is `CVE-2019-5953` and you can see it in the above steps.

![createExemptionVA](createExemptionVA.png)

11. Once you create the exemption, go back to your issue. Since we added the exemption, it shows **OK to Deploy**.

![oktodeployVAexemption](oktodeployVAexemption.png)

## Protecting Sensitive information

Sometimes, you may have sensitive data on your cluster. This may be at application level or cluster level.

At cluster level, all the configuration data will be stored in the etcd component which in turn will be saved on local disk of kubernetes master.

At application level, all the confidential information such as user names, passwords etc. are stored as Kubernetes secrets.

Inorder to protect the etcd data on the local disk of your kubernetes master and also the kubernetes secrets, you can enable IBM Key Protect encryption.

![keyProtectEncryption](keyProtectEncryption.png)

![EnableSecretEncryption](EnableSecretEncryption.png)
