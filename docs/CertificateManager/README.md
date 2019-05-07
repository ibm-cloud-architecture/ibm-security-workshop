# Certificate Manager Lab
## 1. Create the Slack workspace
    
  - Follow this link and join the `IBM_CertMgr` Slack workspace: ``` https://join.slack.com/t/ibmcertmgr/shared_invite/enQtNjE3OTg1MjUzNDYyLWI4ZDUyYzEwYThmYjVhMjY3MDJmZDA3OTNmZmY1ZTlkMmEzNWJiYTNjYTRhNTg1ZDM4MzUwODMzNjdmNzk1N2Y ```
  - **Login** and **verify your account** through the email you provided.
  - **Allow notifications** and join the channel according to the list below
   
  ![join-slack](join-slack.png)

## 2. Create the certificate
  - Open a new Terminal window
  - Go to any folder
  - Run the following commands:
      1. ``` sh ```
      2. ``` mkdir cert ```
      3. ``` cd cert ```
      4. ``` openssl req -x509 -newkey rsa:2048 -subj "/CN=localhost" -keyout myCert.key -out myCert.pem -days 30 -nodes ```

## 3. Configure the Slack notification channel [(docs)](https://cloud.ibm.com/docs/services/certificate-manager?topic=certificate-manager-configuring-notifications#adding-channel)
  1. In the navigation on the service details page, click **Settings**.
  2. Open the **Notifications** tab.
  3. Click **Add Notification Channel**.
  4. Choose **Slack**  as the type of the notification channel.
  5. Enter the **Webhook** matching to your Team ID. **(Found in the table below)**
  6. Click **Save**. A summary of your configuration is displayed.
    ![add-channel](add-channel.png)
  - Import the certificate you created at the previous step (or use the ones under `certs` folder).(https://cloud.ibm.com/docs/services/certificate-manager?topic=certificate-manager-managing-certificates-from-the-dashboard#importing-a-certificate)
    1. Click **Import Certificate**.
    2. Provide a **Certificate Name**. (ie. Slack-Certificate)
    3. Select the **Certificate File** in **PEM** format by clicking **Browse** and finding the certificate files.
    4. Optional: Select the certificate's private key in PEM format by clicking Browse.
    5. Optional: Enter a description.
    6. Click **Import**.

## Slack Channel and webhook:
| ID  | Channel Name            | Webhook   |
| --- | :-----------------------: | ---------: |
| 1   | crtmgr-notification1  | https://hooks.slack.com/services/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 |
| 2   | crtmgr-notification2  | https://hooks.slack.com/services/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 |
| 3   | crtmgr-notification3  | https://hooks.slack.com/services/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 |
| 4   | crtmgr-notification4  | https://hooks.slack.com/services/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 |
| 5   | crtmgr-notification5  | https://hooks.slack.com/services/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 |
| 6   | crtmgr-notification6  | https://hooks.slack.com/services/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 |
| 7   | crtmgr-notification7  | https://hooks.slack.com/services/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 |
| 8   | crtmgr-notification8  | https://hooks.slack.com/services/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 |
| 9   | crtmgr-notification9  | https://hooks.slack.com/services/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 |
| 10  | crtmgr-notification10 | https://hooks.slack.com/services/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 |
| 11  | crtmgr-notification11 | https://hooks.slack.com/services/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 |
| 12  | crtmgr-notification12 | https://hooks.slack.com/services/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 |
| 13  | crtmgr-notification13 | https://hooks.slack.com/services/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 |
| 14  | crtmgr-notification14 | https://hooks.slack.com/services/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 |
| 15  | crtmgr-notification15 | https://hooks.slack.com/services/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 |

