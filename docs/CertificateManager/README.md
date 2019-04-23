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
| 1   | certmgr-notifications1  | something |
| 2   | certmgr-notifications2  | something |
| 3   | certmgr-notifications3  | something |
| 4   | certmgr-notifications4  | something |
| 5   | certmgr-notifications5  | something |
| 6   | certmgr-notifications6  | something |
| 7   | certmgr-notifications7  | something |
| 8   | certmgr-notifications8  | something |
| 9   | certmgr-notifications9  | something |
| 10  | certmgr-notifications10 | something |
| 11  | certmgr-notifications11 | something |
| 12  | certmgr-notifications12 | something |
| 13  | certmgr-notifications13 | something |
| 14  | certmgr-notifications14 | something |
| 15  | certmgr-notifications51 | something |

