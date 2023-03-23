# GameSiteCMS
Exploit Title: GameSiteCMS-File Upload Vulnerability

Date: 2023.3.23

Exploit Author: coco

Vendor Homepage: https://github.com/marekgacek45/GameSite-CMS/commits?author=marekgacek45

Software Link: https://github.com/marekgacek45/GameSite-CMS

A file upload vulnerability has been found in GameSiteCMS, a system for creating game websites. An attacker can successfully get a shell through this vulnerability, with a very serious vulnerability level. Below are the details of the vulnerability.

stay https://gamesitecms.000webhostapp.com/admin/includes/add-image.php?id=1 On the page, users can upload files, but there is no strict verification in the background. Only the file type is limited to $mime_ types = ['image/gif', 'image/png', 'image/jpeg'];， However, this is very dangerous. An attacker can bypass the modification verification by modifying the data packet to successfully upload the file. The uploaded file exists in the https://gamesitecms.000webhostapp.com/uploads An attacker can easily locate and exploit this file under the folder.
