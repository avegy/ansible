Ansible playbooks to install Checkmk agents and enable TLS.
These are useful if you are running Checkmk Raw where most tasks are manual.

checkmk_agent_install_url
This playbook utilizes the Checkmk server URL to download the install the agents. Adjust the site URL to match your environment.

checkmk_agent_install_file
This playbook also installs the agents but uses a local copy of the agent installer.
Use this if your security or network settings don't allow your hosts to download via URL.


At this point you should add the new hosts to Checkmk.  Don't proceed until they show up in the dashboard with the TLS warnings.

checkmk_agent_enable_tls
This will enable TLS on the hosts and register them with the Checkmk server. Adjust playbook.yml to match your site information, agent_registration password, etc.