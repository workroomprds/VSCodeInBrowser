# Set up a server with several web-accessible VSCode instances

* run `droplet_only_setup.yml` to make a droplet
* When it’s up and working (may take babysitting), turn off / make a snapshot / delete
* change the info in `user_setup_and_info.yml`  to refernce the snapshot
* run `user_setup_and_info.yml` to build a server with `vars/users.yml` users
* Each user has a landing page at `«ip_address»/«username»`, and a link to VSCode, using (username and `password`) 
* Details to be found in `access_info.txt`

## Dependencies
Local machine needs `ansible`, ¿`ansible-vault` and ??
Needs a Digital Ocean account for provisioning, and an Anthropic account for `llm`. Neither are hard dependencies.
May need a Cloudflare account or similar to do DNS. Will need ? for certs.

### Secrets
`secrets.yml` needs `do_api_key: «api key»`, `claude_key: «api key»`, 
? possibly `github_token: «token»`, `cloudflare_token: «token»`