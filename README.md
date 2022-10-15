# Deployment 3
## New Purpose
This deployment was to practice the process of deploying a flask app onto a VPC and onto the public subnet
## The Steps
1. We would need an EC2 already with Jenkins
  - If an EC2 is not set up already, you would need to set up the Jenkins service
  - The EC2 should not be in the VPC
2. Create an EC2 into a VPC
  - I had a vpc already made so I just put it in one of the availability zones and in the public subnet
  - You would be expected to make sure that the server has the dependencies, which is in the documentation
3. Followed the documentation to create and configure a jenkins agent
4. Link GitHub to Jenkins
  - Fork the repo with the Flask App
  - Create access token for Jenkins by using GitHub client
    - admin:repo_hook
5. Jenkins Pipeline creation
  - Create a new item which is a multibranch pipeline
  - Add github as a source for the pipeline
  - Validate the source for the pipeline
  - Attempt to build the pipeline given the gitHub repository
## New Additions
This time around, when building the pipeline we also needed to make sure our Jenkins had a plug-in to run. Our Jenkins File had to be altered to have the agent run Gunicorn through the proper port. We also modified the test a bit to make sure it passed. 
## Issues
Documentation was corrected with plugin to keep gunicorn up. There was an issue with the test that was designed to make it fail if not corrected. There was an imbalance in the curly brackets for the jenkins file as well in the pdf documentation. Screenshots of successful build as well as a graph is in the Repository
 
