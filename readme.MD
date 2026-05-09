# Terraform AWS VPC Module Customized
this module is going to create the fallowing resources. for HA first we are going to get first 2 AZ.

* VPC
* Internet gateway associated with VPC
* 2 public subnets
* 2 private subnets
* 2 database subnets
* Database Subnet group
* 1 elastic ip
* 1 nat gateway
* public route table
* private route table
* database route table
* Routes
* route table associations with subnets
* Peering with default vpc if required
* Peering routes in acceptor and requestor route tables
  

  # Inputs
  Project_name (Mandatory) user must supply their project name
  environment (mandatory) user must supply environment
  vpc_cidr (mandatory) user must supply their vpc_cidr
  enable_dns_hostnames (Optional) : defaults to true
  common_tags (Optional) : default is empty user can supply tags in list of strings
  vpc_tags (Optional) 
  igw_tags (Optional)
  public_subnet_cidr (Mandatory) : User Must supply two valid public subnet cidrs
  public_subnet_tags (Optional)

  private_subnet_cidr (Mandatory) : User Must supply two valid private subnet cidrs
  private_subnet_tags (Optional)

  database_subnet_cidr (Mandatory) : User Must supply two valid database subnet cidrs
  database_subnet_tags (Optional)
  
  db_subnet_group (Optional)
  nat_gateway_tags (Optional)

  public_route_table_tags (Optional)
  private_route_table_tags (Optional)
  database_route_table_tags (Optional)

  is_peering_required (Optional) : defaults to true

# Outputs

* vpc_id: VPC_ID created
* public_subnet_ids: public_subnet_ids created
* private_subnet_ids: private subnet ids created
* database_subnet_ids: database subnet ids created
* 