A Docker image based on silvershell/samba that initializes a Samba server
with several shares and DFS links.

Set the environment variables SMB_USER and SMB_PASSWORD to create a user.

The following shares are available:
- /public : Accessible as guest
- /user : Accessible only by users
- /dfs : DFS root

The following DFS links in the /dfs share are available:
- /public : Link to /public share
- /user : Link to /user share
- /firstfail-public : Link with two servers, first will fail, second points to /public share
