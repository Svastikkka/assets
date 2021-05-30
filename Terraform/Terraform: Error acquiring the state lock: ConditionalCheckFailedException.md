(Problem)[https://stackoverflow.com/questions/62189825/terraform-error-acquiring-the-state-lock-conditionalcheckfailedexception]:-  Terraform: Error acquiring the state lock: ConditionalCheckFailedException
# Cause of Error
This error usually appears when one process fails running `terraform plan` or `terraform apply`. For example if your network connection interrupts or the process is terminated before finishing. Then Terraform "thinks" that this process is still working on the infrastructure and blocks other processes from working with the same infrastructure and state at the same time in order to avoid conflicts.

As stated in the error message, you should make sure that there is really no other process still running (e.g. from another developer or from some build-automation). If you force-unlock in such a situation you might screw up your terraform state, making it hard to recover.

# Resolution
If there is no other process still running: run this command

`terraform force-unlock 9db590f1-b6fe-c5f2-2678-8804f089deba`

(where the numerical id should be replace by the one mentioned in the error message)

if you are not sure if there is another process running and you are worried that you might make things worse, I would recommend waiting for some time (like 1h), try again, then try again after maybe 30 min. If the error still persists it is likely that there really is no other process and it's safe to unlock as described above
