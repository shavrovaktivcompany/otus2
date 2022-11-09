1) 

  390  cd terraform/
  391  cat provider.tf 
  392  cat variables.tf 
  393  vim variables.tf 
  394  vim wp.auto.tfvars 
  395  yc config list
  396  yc iam service-account create --name terraform-hw2 --folder-id b1gm001252urmrqt3cvj
  397  yc iam service-account get
  398  yc iam service-account get --id ajet3sfmk9njnbd4sj4i
  399  yc resource-manager folder add-access-binding --id b1gm001252urmrqt3cvj --role editor --service-account-id ajet3sfmk9njnbd4sj4i
  400  yc iam key create --service-account-id ajet3sfmk9njnbd4sj4i --output key.json
  401  ls
  402  pwd
  403  ls /home/user/otus-02/terraform/key.json 
  404  yc iam service-account list
  405  yc iam service-account list --id b1gm001252urmrqt3cvj
  406  yc iam service-account list --help
  407  yc iam service-account list --folder-id b1gm001252urmrqt3cvj
  408  vim wp.auto.tfvars 
  409  vim variables.tf 
  410  vim provider.tf 
  411  vim variables.tf 
  412  vim wp.auto.tfvars 
  413  terraform init
  414  vim network.tf 
  415  terraform apply --auto-approve
  416  vim variables.tf 
  417  vim wp.auto.tfvars 
  418  terraform apply --auto-approve
  419  vim provider.tf 
  420  terraform apply --auto-approve
  421  vim wp.auto.tfvars 
  422  terraform apply --auto-approve
  423  vim wp.auto.tfvars 
  424  terraform apply --auto-approve
  425  vim /home/user/otus-02/terraform/key.json
  426  vim wp.auto.tfvars 
  427  terraform apply --auto-approve
  428  ls
  429  vim wp-app-tf
  430  vim wp-app.tf
  431  terraform apply --auto-approve
  432  ls -la ~/.ssh/
  433  vim wp-app.tf
  434  terraform apply --auto-approve
  435  vim ld.tf
  436  terraform apply --auto-approve
  437  vim db.tf
  438  terraform apply --auto-approve
  439  vim output.tf
  440  terraform apply --auto-approve
  441  terraform destroy --auto-approve
  442  ls
  443  vim ../.gitignore 
  444  ls 
  445  vim README.md
  446  history

