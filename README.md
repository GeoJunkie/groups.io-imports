# groups.io-imports
 Import scripts for Groups.io

This set of import scripts is based on the [Groups.io Yahoo import script](http://lena.kiev.ua/ioimport.zip) from the [Groups.io Group Managers Forum](https://groups.io/g/GroupManagersForum/message/22251). The original Yahoo script here is hers.

# History

2020-03-08: Initial commit with yahoo.ioimpport.pl v7

# Usage Instructions

The basic instructions are the same for all versions. Follow the platform-specific instructions, then follw the below basic instructions using `{platform}.ioimport.pl` wherever you see **Script**.

## Basic Instructions

Your IP-address must have RDNS; your ISP must not block port 25. How to check RDNS: on http://hostip.info there must be something after "Host name:", or else groups.io refuses mail directly from your computer. In such case you can run this program on a web-hosting, invoking it with a web-browser.

This program can be used under Windows, MacOSX, Linux, FreeBSD etc.

1. Create a directory (folder), if under Windows then C:\perl Everything will be in that directory.

2. (only Windows) download to that directory and unzip: (32bit) http://strawberryperl.com/download/5.14.4.1/strawberry-perl-5.14.4.1-32bit-portable.zip or (64bit) http://strawberryperl.com/download/5.14.4.1/strawberry-perl-5.14.4.1-64bit-portable.zip

3. Unzip the ioimport.zip file with this program. And the messages.zip file (containing one or more files) into same directory.

4. Subscribe a new email address to the .io group, in Members set its display name to single dot. Messages from currently non-members and moderated members will be imported with that email address in "From:", original email address inserted into the top of message body

5. From your group on groups.io website in Admin - Members right-click the Download button, save memberlist.csv into the same directory;

6. in Admin - Settings, Moderated must not be checked;

7. in Hashtags press Create Hashtag, enter #mi , check No Email and press Create Hashtag ("mi" means "message import").

8. Run this program (if under Windows then run portableshell.bat in that directory, type perl ioimport.pl and press Enter), it creates needchange.txt file with email addresses from the messages to import which are currently not subscribed to the .io group, or moderated, or have another problematic status.

9. You can optionally create (in the same directory) map.txt file, each line with two email addresses (separated with blanks, tabs or commas): email address in yahooGroup archive (from needchange.txt) and email address of the same person currently subscribed to the .io group.

10. Run the program again, look again into needchange.txt file. You can add to map.txt and run this program again several times.

11. In the same directory create file fromto.txt with one line with two email addresses: the email address you created and subscribed and email address of the .io group or subgroup.

12. Optionally run the program again, it sends an email to +help in order to check that it can email to groups.io directly from your computer (that your ISP doesn't block port 25 and your IP-address has RDNS). The mailbox you subscribed should receive an email with Subject beginning from "Automated help for the".

13. In the same directory create goahead.txt file (with empty content or any content).

14. Run this program again, import begins. If it fails, you can run this program again as many times as needed, it'll skip already imported messages and resume from the failed message.

15. Delete the fromto.txt, goahead.txt and imported.txt files and the files with .mbox. in their names extracted from messages.zip (they would be wrong if you want to import messages from another yahooGroup).

16. On groups.io website in Hashtags under #mi press Edit, Delete, Yes.

## Platform-specific Instructions

* [Yahoo](#yahoo)

### Yahoo

Import yahooGroup messages downloaded from Privacy Dashboard into groups.io via email direct-to-MX. Unzip the download from Privacy Dashboard https://groups.yahoo.com/neo/getmydata (only the file messages.zip is used).
