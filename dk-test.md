# Adding components to Modular BIG-IP (mBIP)


Modular BIG-IP (mBIP) uses a CI/CD integration model that manages code and components through a sequence of repositories (Developer and Image builder). These are integrated into a product at the Bill of materials (BOM).

Most developers doing work in mBIP will work in a Developer repository, working on their individual features. Groups of features are assembled into a service in Image builder repositories into containers. The BOM combines multiple containers and services into a single product image.

This guide will walk you through the steps to build a template project, including a Developer repository, Image builder, and BOM. Developers will most often only need to run through the first task of building a Developer repository, and integrate into a Image builder repository that has been set up by the group.

### Tasks

[Step 1: Create a Developer repository](#step-1:-create-a-developer-repository)

[Step 2: Create an Image builder repository](#step-2:-create-an-image-builder-repository)

[Step 3: Update the Bill of material (BOM) repository with your service(s)](#step-3:-update-the-bill-of-material-bom-repository-with-your-services)

### General prerequisites

Familiarity with the following technologies:

- [GitLab](http://gitlab.com)

- [Docker](https://docker.com)

- [npm](https://npmjs.com)

- [semver](https://docs.npmjs.com/misc/semver)

- [Artifactory](http://artifactory.f5net.com/artifactory/webapp/#/home)

- [Slush](https://github.com/slushjs/slush)



## Step 1: Create a Developer repository


1. Configure your npm environment (one-time only).

   ```
   # make sure you have a ~/.npmrc file
   $ nano ~/.npmrc

   # and add this line to it: registry=http://artifactory.f5net.com/artifactory/api/npm/npm-all/
   ```

2. Create a new repository in the Group [mbip](https://gitlab.f5net.com/mbip). Make sure to follow [naming convention](https://docs.f5net.com/display/PDCSG/Getting+Started%3A+Naming+Conventions) guidelines. Example for a repository name: ``<example-project>``

   **Note**: Further steps for the this task (Step 1: Create a Developer repository) continue to use this same example name for the repository.

   **Important**: Refer to the following table for information about [group members permissions](https://gitswarm.f5net.com/help/user/permissions#group-members-permissions) for creating a repository (and subgroup) in mbip. If you do not have sufficient permission, contact an Owner of mbip to request permission.

   | Gitswarm   | Group | Subgroup    | Project/Repository      |
   | --------   | ----- | --------    | ------------------      |
   | Name used: | mbip  | `<example>` | `<example-project>` |
   | Permission:|       | Owner       | Owner -or- Maintenance  |


3. Before you can run the f5npm slush generator:
   - [Create a new repository](https://docs.gitlab.com/ee/user/project/repository/#create-a-repository) in GitLab.

   - Install [Slush](https://github.com/slushjs/slush) by running the command:

     ```
     $ npm install -g slush
     ```

   - Install the [slush-f5npm](https://gitswarm.f5net.com/mbip/infra/slush-f5npm)    plugin by running the command:

     ```
     $ npm install -g @f5-mbip/f5npm
     ```

   - Ensure you are prepared to enter the following: template name (select ``Developer Repository``), project name/description, main script of project, Git repository path (for your project), and author name/email.


   Run the [f5npm slush generator](https://gitswarm.f5net.com/mbip/infra/slush-f5npm) to create the repository scaffolding.

   The Slush Generator will ask you to answer some questions, and pre-populate some configuration files with those answers.

    ```
    $ git clone git@gitswarm.f5net.com:mbip/<example-project>
    $ cd <example-project>
    $ slush @f5-mbip/f5npm
    ```

   **Important**: When running the commands, make sure to replace ``<example-project>`` with the project name you are using. When answering the question "What is the Git repository path for your project?," make sure to
   include ``mbip/`` before your project name.

4. Push the source code.

   If you need help with basic Git commands, refer to the [GitLab Git Cheat Sheet](https://about.gitlab.com/images/press/git-cheat-sheet.pdf).

5. Assuming that your project was bootstrapped with the f5npm slush generator, you need to release a new version of your project's package.

   Increment the patch component of your version by running the following command:

   ```
   # once code is already merged to master:
   $ npm version patch    # if you made a non-breaking change
   $ # npm version minor  # if you made a minor change
   $ # npm version major  # if you made a breaking change
   ```

6. Verify if the tag created is up-to-date with the new version set in the ``package.json`` file. If the tag is *not* up-to-date, then do the following:

   In your GitLab repository, click **Repository > Tags**, and then click **New tag** to create a new tag to publish to Artifactory.

   **Note**: The tagged version in GitLab should be the same as the version field in the ``package.json`` file. For example, if the ``package.json`` file is showing:

   ```
     {
     . . .
       "version": "1.0.5",
     . . .
     }
   ```

   The tagged version in GitLab should be ``v1.0.5.``


7. Verify **CI / CD > Pipelines** displays the **publish** stage as a result of the tag.

8. Before you can verify the artifacts are in Artifactory:

   - Ensure you have logged in to Artifactory.

   Verify the artifacts are now in Artifactory.

   **Note:** The ``publishConfig`` key in ``package.json`` defines the artifact location.

   **Result:** The source code is in Artifactory and it is ready to be built by the image builder repository.


## Step 2: Create an Image builder repository

1.  Configure your npm environment (one-time only).

    ```
    # make sure you have a ~/.npmrc file
    $ nano ~/.npmrc
 
    # and add this line to it: registry=http://artifactory.f5net.com/artifactory/api/npm/npm-all/
    ```

2. Create a new repository in the Group [mbip](https://gitlab.f5net.com/mbip). Make sure to follow [naming convention](https://docs.f5net.com/display/PDCSG/Getting+Started%3A+Naming+Conventions) guidelines. Example for a repository name: ``<example-img-project>``

   **Note**: Further steps for the this task (Step 2: Create a Developer repository) continue to use this same example name for the repository.

   **Important**: Refer to the following table for information about [group members permissions](https://gitswarm.f5net.com/help/user/permissions#group-members-permissions) for creating a repository (and subgroup) in mbip. If you do not have sufficient permission, contact an Owner of mbip to request permission.

   | Gitswarm   | Group | Subgroup    | Project/Repository      |
   | --------   | ----- | --------    | ------------------      |
   | Name used: | mbip  | `<example>` | `<example-img-project>` |
   | Permission:|       | Owner       | Owner -or- Maintenance  |


3. Before you can run the f5npm slush generator:
   - [Create a new repository](https://docs.gitlab.com/ee/user/project/repository/#create-a-repository) in GitLab.

   - Install [Slush](https://github.com/slushjs/slush) by running the command:

     ```
     $ npm install -g slush
     ```

   - Install the [slush-f5npm](https://gitswarm.f5net.com/mbip/infra/slush-f5npm)    plugin by running the command:

     ```
     $ npm install -g @f5-mbip/f5npm
     ```

   - Ensure you are prepared to enter the following: template name (select ``Image Builder Repository``), project name/description, main script of project, Git repository path (for your project), and author name/email.


   Run the [f5npm slush generator](https://gitswarm.f5net.com/mbip/infra/slush-f5npm) to create the repository scaffolding.

   The Slush Generator will ask you to answer some questions, and pre-populate some configuration files with those answers.

    ```
    $ git clone git@gitswarm.f5net.com:mbip/<example-img-project>
    $ cd <example-img-project>
    $ slush @f5-mbip/f5npm
    ```

   **Important**: When running the commands, make sure to replace ``<example-img-project>`` with the project name you are using. When answering the question "What is the Git repository path for your project?," make sure to
   include ``mbip/`` before your project name.


4.  Update the repository (that you previously created) to reference the source code of your project.

    ```
    $ cat package.json
    ...
     "dependencies": {
       "@f5-mbip/<example-img-project>": "^1.1.1"
      },
    ```  

5. Update ``Dockerfile``, and then push to Git.

   ```
   $ git add .
   $ git commit -m "Initial commit"
   $ git push origin master
   ```

6. Release your image.

   ```
   $ git checkout master
   $ git pull
   $ npm version patch     # substitute "minor" or "major" as appropriate
   ```

   **Note**: For more information about patch, major, and minor:

   - [mBIP SDLC > Versioning](https://gitswarm.f5net.com/mbip/docs/blob/master/sdlc.md).


7. Verify **CI / CD > Pipelines** displays **publish** as a result of the tag.
8. Verify the artifacts are now in Artifactory.
9. Verify the built image is in Artifactory.

   **Note:** ``f5-mbip-docker`` is the Modular BIG-IPs Docker registry. The f5 key in ``package.json`` defines the image location.


   **Result:** The built image is in Artifactory.


## Step 3: Update the Bill of material (BOM) repository with your service(s)


1. Before you can update the yaml file(s), find the appropriate yaml file for your service in the [repository](https://gitlab.f5net.com/mbip/mbip-bom/tree/master/bom).

   **Note**: Contact the SME in your area for more specific guidance about selecting a yaml file.

   On a feature branch, update the yaml file(s) in the BOM  repository.

   ```
   $ git clone git@gitswarm.f5net.com:mbip/mbip-bom.git
   $ cd bom

   ### Perhaps add your image into a yaml file in bom directory. Below is just an example.
   . . .
   services:
    my-demo:
     image: artifactory.f5net.com/f5-mbip-docker/img-<example-project>:0.1
   . . .
   ```

2. Create a merge request to merge all changes to the master branch.

3. Run the following commands to release the BOM.

   ```
   $ git checkout master
   $ git pull
   $ npm version patch     # substitute "minor" or "major" as appropriate
   ```

4. Run the following commands to upgrade the ``mbip-installer``.

   ```
   $ git clone git@gitswarm.f5net.com:mbip/mbip-img-installer.git
   $ cd mbip-img-installer
   $ git checkout -b upgrade-installer
   $ npm upgrade
   $ git commit -m 'upgrading installer image'
   $ git push
   $ git checkout master
   $ npm version patch    # substitute "minor" or "major" as appropriate
   ```

5. Deploy a new virtual machine (VM). Refer to the task "Creating a Modular BIG-IP instance in VIO."
