# Certificate Manager Lab
1) Create the Slack workspace
   - Follow this link and join Slack workspace - https://join.slack.com/t/ibmcertmgr/shared_invite/enQtNjE3OTg1MjUzNDYyLWI4ZDUyYzEwYThmYjVhMjY3MDJmZDA3OTNmZmY1ZTlkMmEzNWJiYTNjYTRhNTg1ZDM4MzUwODMzNjdmNzk1N2Y
   - Login
   - Allow notifications and join the channel according to the list below
   ![join-slack](join-slack.png)
2) Create the certificate
   - Open a new Terminal window
   - go to any folder
   - run the following commands
   ```sh
    mkdir cert
    cd cert
    openssl req -x509 -newkey rsa:2048 -subj "/CN=localhost" -keyout myCert.key -out myCert.pem -days 30 -nodes

2) Open a new tab and navigate to cloud.ibm.com 
   - Create a new instance of CertMgr (https://cloud.ibm.com/catalog/services/certificate-manager)
   - Configure the Slack notification channel (https://cloud.ibm.com/docs/services/certificate-manager?topic=certificate-manager-configuring-notifications#adding-channel)
   - Import the cert and wait 1 min to get the notification (https://cloud.ibm.com/docs/services/certificate-manager?topic=certificate-manager-managing-certificates-from-the-dashboard#importing-a-certificate)


## Slack Channel and webhook:
| ID  | Channel Name            | Webhook   |
| --- | ----------------------- | --------- |
| 1   | crtmgr-notification1  | https://hooks.slack.com/services/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 |
| 2   | crtmgr-notification2  | https://hooks.slack.com/services/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 |
| 3   | crtmgr-notification3  | https://hooks.slack.com/services/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 |
| 4   | crtmgr-notification4  | something |
| 5   | crtmgr-notification5  | something |
| 6   | crtmgr-notification6  | something |
| 7   | crtmgr-notification7  | something |
| 8   | crtmgr-notification8  | something |
| 9   | crtmgr-notification9  | something |
| 10  | crtmgr-notification10 | something |
| 11  | crtmgr-notification11 | something |
| 12  | crtmgr-notification12 | something |
| 13  | crtmgr-notification13 | something |
| 14  | crtmgr-notification14 | something |
| 15  | crtmgr-notification15 | something |

