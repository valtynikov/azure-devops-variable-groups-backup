## Azure DevOps YAML pipeline to backup variable groups to a Git repo

Easily backup your Azure DevOps variable groups to a Git repo on a scheduled basis using this YAML pipeline. Use the commit history to see what changed, when, and by whom.

- Each variable group, including all metadata and variables, saved as a seprate JSON file
- The **Modified by** user for each variable group is associated with the commit by the backup process
- The default schedule is set to run every 15 minutes Mon-Fri between 9am and 5pm (UTC-05:00)

## Setup

1. Create a new Git repo in your Azure DevOps project
2. Grant the **Project Collection Build Service** _Contribute_ permission to the Git repo<sup>1</sup>
3. Commit the `azure-pipelines.yml` to the repo
4. Create a new pipeline using the `azure-pipelines.yml` file
5. Adjust the pipeline schedule as desired <sup>2</sup>

<sup>1</sup> https://docs.microsoft.com/en-us/azure/devops/pipelines/scripts/git-commands?view=azure-devops&tabs=yaml#grant-version-control-permissions-to-the-build-service

<sup>2</sup> https://docs.microsoft.com/en-us/azure/devops/pipelines/process/scheduled-triggers?view=azure-devops&tabs=yaml

## More

For additional details, please refer to my blog post: https://www.blendmastersoftware.com/blog/azure-devops-variable-groups-backup
