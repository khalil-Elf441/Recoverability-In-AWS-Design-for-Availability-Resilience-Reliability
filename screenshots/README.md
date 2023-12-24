# Data durability and recovery

In this project you will create highly available solutions to common use cases.  You will build a Multi-AvailabilityZone, Multi-Region database and show how to use it in multiple geographically separate AWS regions.  You will also build a website hosting solution that is versioned so that any data destruction and accidents can be quickly and easily undone.
### Part 1
Complete the following steps:
### Data durability and recovery

Screenshots of both VPCs after they are created.

![primary_Vpc](/screenshots/primary_Vpc.png)

![secondary_Vpc](/screenshots/secondary_Vpc.png)

### Highly durable RDS Database

Screenshots of the configuration of the databases in the active and secondary region after they are created.
Screenshots of the configuration of the database subnet groups as well as route tables associated with those

![primaryDB_config](/screenshots/primaryDB_config.png)

![primaryDB_config](/screenshots/primaryDB_config_backups_enabled.png)

![secondaryDB_config](/screenshots/secondaryDB_config.png)

![primaryDB_subnetgroup](/screenshots/primaryDB_subnetgroup.png)

![secondaryDB_subnetgroup](/screenshots/secondaryDB_subnetgroup.png)

![primaryVPC_subnets](/screenshots/primaryVPC_subnets.png)

![secondaryVPC_subnets](/screenshots/secondaryVPC_subnets.png)

![primary_subnet_routing](/screenshots/primary_subnet_routing.png)

![secondary_subnet_routing](/screenshots/secondary_subnet_routing.png)

### Estimate availability of this configuration
Write a paragraph or two describing the achievable Recovery Time Objective (RTO) and Recovery Point Objective (RPO) for this Multi-AZ, multi-region database in terms of:

1. Minimum RTO for a single AZ outage
2. Minimum RTO for a single region outage
3. Minimum RPO for a single AZ outage
4. Minimum RPO for a single region outage

Answers in a text file named "estimates.txt"

### Demonstrate normal usage

The log of connecting to the database, creating the table, writing to and reading from the table in a text file called "log_primary.txt"

### Monitor database

Screenshots of the DB Connections and the database replication configuration. Name your screenshots: monitoring_connections.png, monitoring_replication.png

![monitoring_connections](/screenshots/monitoring_connections.png)

![monitoring_replication](/screenshots/monitoring_replication.png)

![monitoring_replication](/screenshots/monitoring_replication_config.png)


### Part 2
### Failover And Recovery



Log of connecting to the database, writing to and reading from the table in a text file called "log_rr_before_promotion.txt"

Screenshot of the database configuration now, before promoting the read replica database in the next step.

![rr_before_promotion](/screenshots/rr_before_promotion.png)

Promote the read replica


Log of connecting to the database, writing to and reading from the database in a text file named "log_rr_after_promotion.txt"

Screenshots of the database configuration after the database promotion.

![rr_after_promotion](/screenshots/rr_after_promotion.png)


### Part 3
### Website Resiliency

Build a resilient static web hosting solution in AWS. Create a versioned S3 bucket and configure it as a static website.

Screenshot of the webpage. Name your screenshot "s3_original.png"

![s3_original](/screenshots/s3_original.png)

You will now “accidentally” change the contents of the website such that it is no longer serving the correct content


Screenshot of the modified webpage. Name your screenshot "s3_season.png"

![s3_season](/screenshots/s3_season.png)


You will now need to “recover” the website by rolling the content back to a previous version.

Screenshot of the modified webpage. Name your screenshot "s3_season_revert.png"

![s3_season_revert](/screenshots/s3_season_revert.png)

You will now “accidentally” delete contents from the S3 bucket. Delete “winter.jpg”

Screenshots of the modified webpage and of the existing versions of the file showing the "Deletion marker". Name your screenshots: s3_deletion.png, s3_delete_marker.png

![s3_deletion](/screenshots/s3_deletion.png)

![s3_delete_marker](/screenshots/s3_delete_marker.png)


You will now need to “recover” the object.

Screenshot of the modified webpage. Name your screenshot "s3_delete_revert.png"

![s3_delete_revert](/screenshots/s3_delete_revert.png)


## License
