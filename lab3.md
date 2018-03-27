## E-mail client

Use application-level protocols (POP3/IMAP and SMTP) to implement an email client with basic functionality.


### Prerequisites

- Read about OSI model (definition, basic info)
- Read about (de)serialization, parsing
- Client-Server architecture


## Tasks

#### How to implement this lab

The entrypoint of this lab is the base task.
Each next task is based on previous one and has a corresponding grade.
If you implement tasks for a certain grade, you have to prove by answering question related to implementation and lab's theme.

### Base task (5 - 6)

There are some prerequisites:
- pick up an e-mail service (it should support IMAP/POP3 and SMTP clients),
- ...

Implement a simple mail client which offers the following features:
- Log in;
- Get number of unread messages;
- Get last N received messages (display subject, date, sender), ordered by date;
- Send a message. Next fields must be available - subject, recipient, CC, body;

### Message Preview and MIME-types (7)

- Display additional info for messages list:
  - If there're attachments in the e-mail, display number of attached files;
  - If message is plain text, display a short preview of the message (e.g. first sentence);
- Allow to select and read a message (just display content)

### IMAP, HTML and attachments (8)

- If you implemented previous task using POP3 protocol, migrate the app to IMAP;
- Allow to send e-mail with attachments (any file, at least 1 attachment);
- If an e-mail is in HTML format, either display it using a WebView or send as file and open in browser;
- Implement drafts (synchronized with the e-mail server)

### Notifications and search (9)

- Check in background for new messages and display a notification (show pop-up and/or play a sound) when there's a new message;
- Add search feature (e.g. find messages which contain a <keyword> in subject or sender).
- Add "remember me" option to the login screen (store passwords **securely**).

### UX improvements (10)

- "Undo" button - allow to undo sending a message after user sent it (implementation is up to you);
- Implement pagination for messages (e.g. display 10 msg per page with next/prev buttons)
- Allow basic formatting (bold, italic etc) for a new email.
- If there's no internet connection, enqueue messages and send them later.
