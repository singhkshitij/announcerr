# Announcerr Github Action

Automatically announce and send mails to list of subscribers on every product release 🚀 

## Usage

```yaml
- name: Announcerr
  uses: singhkshitij/announcerr@v2
  with:
    server_address: smtp.gmail.com
    server_port: 465
    username: ${{secrets.MAIL_USERNAME}}
    password: ${{secrets.MAIL_PASSWORD}}
    subject: Github Actions job result
    # Literal body:
    body: Build job of ${{github.repository}} completed successfully!
    # Read file contents as body:
    body: file://README.md
    to: obiwan@tatooine.com,yoda@dagobah.com
    from: Luke Skywalker # <user@example.com>
    # Optional content type (defaults to text/plain):
    content_type: text/html
    # Optional attachments:
    attachments: attachments.zip,git.diff,./dist/static/main.js
```
