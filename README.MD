### AWS VPC module

This module creates following resources.
* VPC
* Internet Gateway with VPC association
* 2 Public Subnets in 1a and 1b
* 2 Private Subnets in 1a and 1b
* 2 Database Subnets in 1a and 1b
* Elastic IP
* NAt gateway in 1a Public Subnet
* Public Route Table
* Private Route Table
* Database Route Table
* Subnets and Route table associations
* VPC peering if user requests
* Adding the peering route in default VPc, if user dont provide acceptor VPC explicitly. 
* Adding the Peering routes in public, private and database route tables

### Inputs

* project_name (requiresd) - your project name
* environment (required) - which environment you are working in
* VPC_cidr (optional) - Default value is 10.0.0.0/16, user can override
* enable_dns_hostnames (optional) - Default value is true
* common_tags (optional) -Better to provide
* VPC_tags (optional)
* igw _tags (optional)
*  public_subnets_cidr (Required) - user must provide 2 valid public subnets CIDR
* public_subnets_tags (optional)
* private_subnets_cidr (Required) - user must provide 2 valid private subnets CIDR
* Private _subnets_tags (optional)
* databse_subnets_cidr (Required) - user must provide 2 valid database subnets CIDR
* Database_subnets_cidr (optional)
* nat_gateway_tags (optional)
* Public_route_table_tags (optional)
* Private_route_table_tags (optional)
* database_route_table_tags (optional)
* is_peering_required  (optional) - default value is false
* acceptor_vpc_id (optional) - default value is default vpc ID
* vpc_peering_tags (optional) - Default value is empty. type is map

### Outputs
* vpc_id - vpc ID created
* public_subnet_ids - 2 public subnet ID created
* private_subnet_ids - 2 private subnet ID created
* database_subnet_ids - 2 database subnet ID created

