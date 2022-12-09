# PROJECT: Holberton Sandbox Initializer

AUTHOR: Matthew Allen

## DESCRIPTION

This is a project consists of a configuration file (`.bashrc`) and a bash script (`sandbox_initializer`) which is used to set up a new Ubuntu Sandbox for use with Holberton School's curriculum.

Such a script significantly simplifies sandbox setup for students starting sandboxes.

## USAGE

To use this script, you first must fork this repository, then clone it to your new sandbox.

### `sandbox_initializer`
To execute the script, run the following command:

```
./sandbox_initializer {token} {github username} {github email}
```

* `{token}` refers to your GitHub Personal Access Token (classic).
* `{github username}` refers to your GitHub username, strangely enough.
* `{github email}` refers to the email you used for GitHub.

This will not set the remote origin url.  When you attempt to push to a repo, use the following command within the repo you're pushing from:

```
git remote set-url origin https://{username}:{token}@github.com/{username}/{reponame}.git
```

### `AirBnB_sandbox_initializer`
To execute the script, run the following command:

```
./AirBnB_sandbox_initializer {token} {github username} {github email}
```

This script does the same as above, however, it sets up your MySQL server with the tables, users, and entries used for Holberton's AirBnB project.

This script _does_ set the remote origin url, so performing a `git push` should be successful for the `holbertonschool-AirBnB_clone_v4` repository.


## Customization & Extra Functionality

By default, the only repository that is cloned is the `holbertonschool-AirBnB_clone_v4`.
To add more repositories, duplicate line 12 of the `sandbox_initializer` file and replace the repository name with the name of the desired repo.
There are already some git clone commands commented out.  Simply uncomment these lines if you wish to clone these repos.

At the bottom of the `.bashrc` file, there are three commented out variable declarations - one for each of the web-servers provided by holberton (web01, web02, lb01).  These are variables created to hold the IP addresses of your web servers for simple access.  Change these IP addresses to that of each corresponding server.  This will allow you to use these variables wherever you would normally use them in bash by prepending a `$` to the name of the desired server.

>Ex: `echo $web01` prints `0.0.0.0` (update this to your server's IP address)

## AUTHOR:

### Matthew Allen 

* [GitHub](https://github.com/mdallen5393)
* [LinkedIn](https://www.linkedin.com/in/itsmatthewallen/)
