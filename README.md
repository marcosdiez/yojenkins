<h1 align="center">yo-jenkins</h1>

<!-- [![Testing, Building, and Publishing](https://github.com/ismet55555/yo-jenkins/actions/workflows/test-build-publish.yml/badge.svg?branch=main)](https://github.com/ismet55555/yo-jenkins/actions/workflows/test-build-publish.yml) -->

`yo-jenkins` is a command line interface (CLI) tool to monitor, manage, and have fun with a Jenkins server.  

**NOTE:** *This tool is in **pre-alpha** release phase. Please report any issues, odd behavior, or suggestions. Read more about the [release cycle](https://en.wikipedia.org/wiki/Software_release_life_cycle).*

&nbsp;

# Installation

1. Install system dependencies for `simpleaudio` sound Python package
   - | Platform 	| Command                                                                        	|
     |----------	|--------------------------------------------------------------------------------	|
     | MacOS    	| Not needed                                                                     	|
     | Windows  	| Not needed                                                                     	|
     | Ubuntu   	| `sudo apt update && apt-get install -y python3-dev python3-pip libasound2-dev` 	|
     | CentOS   	| `sudo yum update && yum install -y python3-devel gcc alsa-lib-devel`           	|


2. Install `yo-jenkins`
    - Depending on your access rights, you may need to add `--user` to the below commands
    - **Option 1:** From Python Package Index (PYPI) using `pip`
      - ```bash
        pip install yo-jenkins
        ```

   - **Option 2:** Download all files in this GitHub repository and install using the included `setup.py`
     - ```bash
         python setup.py install

        # OR

         pip install .
         ```

&nbsp;

# Jenkins Plugin Requirements

The following Jenkins plugin are required for `yo-jenkins` to use all its functionalities. In order to install a plugin, go to *Manage Jenkins > Manage Plugins > Available*
- [Folders](https://plugins.jenkins.io/cloudbees-folder/) (cloudbees-folder)
- [Next Build Number](https://plugins.jenkins.io/next-build-number/) (next-build-number)
- [Promoted Builds](https://plugins.jenkins.io/promoted-builds/) (promoted-builds)

&nbsp;

# Local Jenkins Server Setup Using Docker

`yo-jenkins` offers an easy way to quickly set up a local Jenkins server within a Docker container. This server is setup and ready to go to tinker with `yo-jenkins`. 

**NOTE:** You must have Docker on running. See [Docker installation guide](dev_things\docker.md).

Run the following command to set up a local Jenkins server:
```bash
yo-jenkins server server-deploy
```

Use `--help` for available options, and use `--debug` to troubleshoot any issues.

&nbsp;

# Main Menu

```txt

Usage: __main__.py [OPTIONS] COMMAND [ARGS]...

                        YO-JENKINS (Version: 0.0.0) 

  yo-jenkins is a tool that is focused on interfacing with Jenkins server from
  the comfort of the beloved command line.  This tool can also be used as a
  middleware utility, generating and passing Jenkins information or automating
  tasks.

  QUICK START:

      1. Configure yo profile:  yo-jenkins auth configure

      2. Add yo API token:      yo-jenkins auth token --profile <PROFILE>

      3. Verify yo creds:       yo-jenkins auth verify

      4. Explore yo-jenkins

Options:
  -v, --version  Show the version
  --help         Show this message and exit.

Commands:
  auth     Manage authentication and profiles
  build    Manage builds
  folder   Manage folders
  job      Manage jobs
  node     Manage nodes
  server   Manage server
  stage    Manage build stages
  step     Manage stage steps
  tools    Tools and more

```

&nbsp;

# Report Bugs and Issues
As with any other software, issues do come up during various usage scenarios that may not be accounted for during development and testing. **Help from real users is enormously helpful.**

Please report and bugs and odd behaviors to [GitHub Issues](https://github.com/ismet55555/yo-jenkins/issues/new?assignees=&labels=&template=bug_report.md&title=). If possible, please include the command that caused the issue with `--debug`. For example:

```bash
yo-jenkins server server-deploy --debug
```

&nbsp;

# Contributors
**Ismet Handžić** - GitHub: [@ismet55555](https://github.com/ismet55555)

&nbsp;

# Licence
This project is licensed under the *GNU General Public License Version 3* License. Please see the [LICENSE](LICENSE) file for details. Also a complete [history of this licence](https://en.wikipedia.org/wiki/GNU_General_Public_License).