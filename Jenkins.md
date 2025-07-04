Q: Can you explain the CICD process in your current project ? or Can you talk about any CICD process that you have implemented ?

--> 
Have ypu written any pipelines and can you write a example pipeline

Git checkout
Compile
Test 
Trivy FS Scan
Sonar Analysis
Build Application
Publish Artifacts
Docker Build & tag
trivy Image Scan
Docker Push
k8s Deploy
=================>>>>




Pipeline {
    agent any

    enviroment{

    }
    
    stages{
        steps('Git Checkout'){

        }
    }

    stages{
        steps('compile'){

        }
    }

    stages{
        steps('Unit test'){

        }
    }

    stages{
        steps('trivy FS Scan'){

        }
    }

    stages{
        steps('Sonar Analysis'){

        }
    }

    stages{
        steps('Build Application'){

        }
    }

    stages{
        steps('Publish Artifacts'){

        }
    }

    stages{
        steps('Docker Build & Tag'){

        }
    }

    stages{
        steps('Trivy image scan'){

        }
    }

    stages{
        steps('Docker Push'){

        }
    }

    stages{
        steps('K8s Deploy'){

        }
    }

}

=========================================>>>>> 

Q: What are the different ways to trigger jenkins pipelines ?

Ans:->  There are many ways to trigger the jenkins pipe lines

1. Poll SCM
2. Build Triggers
3. webhooks
======================================================>>>

Q: How to backup Jenkins ?
Ans :-> 


Q: How do you store/secure/handle secrets in Jenkins ?

Ans :->  there are multiple ways to acheive this
1. Credientials plugins
2. Enviroment variables
3. hashicrop Vault
4. Thrid party Secreat Mangement.

Q: What is latest version of Jenkins or which version of Jenkins are you using ?

Ans :-> I used Jenkins LTS version

Q. What is shared module?
Ans:-> A Shared Library is a Git repository (or part of one) that contains reusable Groovy code you can include in Jenkins pipelines using the @Library annotation.

Q: can you use Jenkins to build applications with multiple programming languages using different agents in different stages ?

Ans :->Yes, Jenkins can be used to build applications with multiple programming languages by using different build agents in different stages of the build process.

Q: How to setup auto-scaling group for Jenkins in AWS ?

Ans :->

Launch EC2 instances
2. Create Launch configurations
3. Create auto scalling group
4. configure scalling policy
5. Load balancer
6. connect to jenkins
7. Monitoring instances 

Q. How to add a new worker Node in jenkins?
A: Log into the Jenkins master and navigate to Manage Jenkins > Manage Nodes > New Node. Enter a name for the new node and select Permanent Agent. Configure SSH and click on Launch.

Q: How to add a new plugin in Jenkins ?

A: Using the CLI, java -jar jenkins-cli.jar install-plugin <PLUGIN_NAME>

Using the UI,

Click on the "Manage Jenkins" link in the left-side menu.

Click on the "Manage Plugins" link.

Q. Q: What is JNLP and why is it used in Jenkins ?

Ans :-> JNLP (Java Network Launch Protocol) in Jenkins is used to connect inbound agents (also called "JNLP agents") to the Jenkins controller.

Q.What jenkins pluggins do you use daily ?
Ans:-> git pluggin, github pluggin, docker pluggin,kubernetes pluggin, sonarpluggin, maven pluggin,

=========================================================>>>>


What’s the difference between continuous integration, continuous delivery, and continuous deployment?

A. CI -> Developers regularly merge code changes into a shared repository. Automated tests run to catch issues early.
CD :-> Every successful build from CI is automatically prepared for release. Manual approval is still needed before pushing to production.
CD :-> - Like Continuous Delivery, but no manual approval — code that passes tests is automatically deployed to production.

CI → test automatically
CD → ready to release
Continuous Deployment → released automatically

Benefits of CI/CD
Ans :-> - Faster releases, - Improved code quality, - Reduced manual work 🤖, - Quick recovery


What is meant by CI-CD?
Ans :->  - CI 🧪: Automatically tests code as developers merge it, catching bugs early.
- CD 🚀: Automatically prepares (and sometimes deploys) tested code to production.
In a nutshell: it’s about shipping better software, faster, and with fewer headaches. Want to see how you could use it in a real project setup?


What is Jenkins Pipeline?
Ans :-> A Jenkins Pipeline is a way to automate your software delivery process in Jenkins using code.

How do you configure the job in Jenkins?
Where do you find errors in Jenkins?
Ans :-> Ans :-> - Console Output 🖥️, - Go to the job → click the failed build → check Console Output 


In Jenkins how can you find log files?
Ans :-> - Go to Manage Jenkins → System Log for real-time and custom logs

Jenkins workflow and write a script for this workflow?
Ans :-> A typical Jenkins workflow automates the build → test → deploy cycle. Here's a common flow:
- Checkout Code from Git
- Build the application (e.g., using Maven, npm, etc.)
- Run Tests (unit/integration)
- Package Artifacts (e.g., JAR, Docker image)
- Deploy to staging or production



Is Only Jenkins enough for automation?
Ans :-> Not Quite, Jenkins is powerful but not always enough for automations. you will still  need docker k8s git ansible terraform etc. tools

Explain diff stages in CI-CD setup
Ans :-> git checkout, Build , Test, Package, Deploy, Monitor 

Name some of the plugins in Jenkin?

Ans :-> doker, k8s, git, githuub, sonarscanner, junit,
