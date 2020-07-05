https://medium.com/@pmvk/google-cloud-automating-installations-with-deployment-manager-and-ansible-712d096d9108


Google deployment manager allows one to create a set of declarative templates to deploy cloud platform resources consistently. It uses 3 types of files primarily:
A configuration file which is a YAML file and defines your resources such as instance type, disk configuration, subnet to use, zones etc.
2. Template files which can be Jinja templates or Python scripts. To include these templates as part of the configuration, you import them.
3. Schema file which can be used to enforce how users can interact with templates
