docker-openstack-clients
========================

OpenStack command line clients in a Docker container.

After pulling the image from the index repository run a container
passing through the OpenStack environment variables. 

    $ docker run -e OS_AUTH_URL=$OS_AUTH_URL \
        -e OS_REGION_NAME=$OS_REGION_NAME \
        -e OS_TENANT_NAME=$OS_TENANT_NAME \
        -e OS_USERNAME=$OS_USERNAME \
        -e OS_PASSWORD=$OS_PASSWORD \
        -t -i --rm booleancandy/openstack-clients nova flavor-list
    +-----+------------------+-----------+------+-----------+------+-------+-------------+-----------+
    | ID  | Name             | Memory_MB | Disk | Ephemeral | Swap | VCPUs | RXTX_Factor | Is_Public |
    +-----+------------------+-----------+------+-----------+------+-------+-------------+-----------+
    | 100 | standard.xsmall  | 1024      | 10   | 10        |      | 1     | 1.0         | N/A       |
    | 101 | standard.small   | 2048      | 30   | 10        |      | 2     | 1.0         | N/A       |
    | 102 | standard.medium  | 4096      | 30   | 50        |      | 2     | 1.0         | N/A       |
    | 103 | standard.large   | 8192      | 30   | 130       |      | 4     | 1.0         | N/A       |
    | 104 | standard.xlarge  | 15360     | 30   | 270       |      | 4     | 1.0         | N/A       |
    | 105 | standard.2xlarge | 30720     | 30   | 470       |      | 8     | 1.0         | N/A       |
    | 110 | standard.4xlarge | 61440     | 30   | 870       |      | 12    | 1.0         | N/A       |
    | 114 | standard.8xlarge | 122880    | 30   | 1770      |      | 16    | 1.0         | N/A       |
    | 203 | highmem.large    | 16384     | 30   | 130       |      | 4     | 1.0         | N/A       |
    | 204 | highmem.xlarge   | 30720     | 30   | 270       |      | 4     | 1.0         | N/A       |
    | 205 | highmem.2xlarge  | 61440     | 30   | 540       |      | 8     | 1.0         | N/A       |
    +-----+------------------+-----------+------+-----------+------+-------+-------------+-----------+
