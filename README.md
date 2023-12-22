# README

## Installation

To run the imapsync tool using Docker, follow the steps below:

- Clone Repository:
git clone https://github.com/diego-mascarenhas/imapsync.git

- Navigate to Repository Directory:
cd imapsync

- Start Docker Containers:
docker-compose up -d

- Access Container Bash:
docker exec -it mailsync-imapsync-1 bash


## Usage

Inside the container, use the imapsync tool with the following command:

imapsync \
    --host1 server1.imap.tld --user1 mailbox@email.tld --password1 'password1' \
    --host2 server2.imap.tld --user2 mailbox@email.tld --password2 'password2'

Replace the placeholder values with your actual IMAP server details and mailbox credentials.


## Notes

- Ensure that Docker and Docker Compose are installed on your machine before running the above commands.

- There is no need to expose any ports explicitly in the container. The necessary port configurations are handled internally within the Docker network.

- Be cautious when using passwords with special characters, as they might cause authentication errors. If you encounter authentication issues, consider using passwords without special characters or ensure proper escaping.