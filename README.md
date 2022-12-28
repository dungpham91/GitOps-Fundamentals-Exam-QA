# GitOps-Fundamentals-Exam-QA
Summary of questions and answers when taking Codefresh's GitOps Fundamentals test.

1. `What is GitOps?` -> It is a set of best-practices for deployments.

2. `How are GitOps and DevOps related?` -> DevOps is a paradigm/mindset. GitOps is a set of best practices.

3. `Is the following statement true or false?` -> GitOps is only for Kubernetes applications. - False

4. `What is the major advantage of GitOps?` -> Eliminating configuration drift.

5. `What is a major disadvantage of GitOps?` -> GitOps handles only deployments

6. `What is Argo CD?` -> A GitOps Agent

7. `Which other Argo products does Argo CD need to function correctly?` -> None. Argo CD is a standalone project. It works great with the other Argo projects, but it does not depend on them.

8. `How does ArgoCD interact with clusters?` -> You can have any combination of clusters and ArgoCD instances. ArgoCD can deploy applications on the cluster it is installed on, or other external clusters that are authenticated correctly

9. `How can you install ArgoCD on your cluster?` -> You can use any of the above including other community methods

10. `What is the relationship between the ArgoCD Web interface and the Argo CD Command line executable?` -> The Argo CD UI and the CLI can be used interchangeably according to your needs.

11. `Is the following statement true or false?` -> If you have enabled the "auto-sync" option in an Argo CD application and something is changed manually in the cluster, then Argo CD will automatically discard the change. - False

12. `Is the following statement true or false?` -> If you have enabled the "auto-sync" option in an Argo CD application and you delete a resource in Git, then Argo CD will automatically delete that resource from the cluster as well. - False

13. `What is the proper way to handle application secrets via GitOps?` -> Encrypt them and store them in Git. Then decrypt them during runtime.

14. `If you use Bitnami Sealed Secrets, then where does encryption and decryption take place?` -> Encryption happens via the kubeseal executable. Decryption happens via the Sealed Secrets controller.

15. `You have just logged in the Argo CD UI and created an application using a Git repository that holds your Helm chart. You sync the application, and everything is fine. What is the next step that you should take?` -> Create a declarative file of the application and other resources (e.g. Argo CD project) used and store them in Git.

16. `You just created a Helm application using the Argo CD web interface. Now you go the command line and you enter helm list. To your surprise nothing is printed.` -> The helm command will never work no matter what you do in Argo CD

17. `What kind of applications can Argo CD deploy?` -> ArgoCD can deploy all of the above

18. `What is Progressive Delivery?` -> A way to gradually deploy applications minimizing downtime

19. `What is Argo Rollouts` -> A Kubernetes controller for progressive delivery

20. `What is the relationship between Argo CD and Argo Rollouts` -> Argo CD and Argo Rollouts can either be deployed individually or both at the same time.

21. `What are Blue/Green deployments?` -> A deployment method where the new version is launched while the old version is still running. Both version exist during the deployment

22. `What are Canary deployments` -> A deployment method where only a subset of live users get access to the new version of the application

23. `How does Argo Rollout work?` -> You need to convert your Kubernetes Deployment to a Rollout resource to enable progressive delivery
