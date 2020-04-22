# Node cookbook 🏠💻👩‍💻


This cookbook was created in the aim of creating an image with NodeJs installed on it.

- This cookbook installs NodeJs from the source.

- It creates its apt package and then installs it.

- The recipe also creates the config files and the service file with dynamic input of variables.

### What is Chef
Chef is a declarative configuration management and automation platform used to manages the infrastructure by writing code rather than using a manual process so it enables organisations or individuals to generate a process with better testing, efficient and predictable deployments, centralised versioning, and reproducible environments across all your servers.

Moreover, Chef supports multiple platforms like Windows, Ubuntu, Centos, and Solaris etc. It can also be integrated with cloud platform like AWS, Google Cloud Platform, and Open Stack etc.

This cookbook was created in the aim of creating an image with Node installed on it.


When creating a new Chef cookbook, it will automatically create certain directories and files. Then it will be apple to adding your custom files on top these default files and directories. For every chef cookbook you create, you’ll see 8 directories and 3 files under the top-level for that particular cookbook.


## NodeCookbookStarterCode
This cookbook was created using chef generate cookbook MongoCookbookStarterCode to have mongo installed. It also contains a Berksfile which has the chef supermarket and the metadata and is used to manage the dependencies of the cookbook and a berks-cookbooks berks vendor.

### Verifying chef version

• verifying the Chef development kit version using the following command:

```
chef --version
```

### Create a repo

• Create a repo to store the cookbooks, data bags and other chef related folders using the chef generate command:

- Generate cookbook:

```
chef generate repo <name>
```
••• <name> is the custom name given by the user for example in this task called NodeCookbookStarterCode

- Running Kitchen

```
   kitchen create
```
-  Run provision from recipe
- runs all recipes

```
kitchen converge
```

- Prepare for testing

 • run setup

```
kitchen setup
```
-  Run tests:

```
kitchen verify
```
Destroy machine

```
kitchen destroy
```
Run all above ?
kitchen create --> all the steps --> kitchen destroy?

```
kitchen test

```

## List of what Installs:

• NodeJs

• Nginx

• pm2 and npm


### Test Locally
- Running my unit test:

```
chef exec rspec
```
- Running integration tests and closing machine:

```
kitchen tests
```

## Tests in AWS
- Running integration tests in AWS

```
KITCHEN_YAML=kitchen_cloud.yml kitchen test
```
