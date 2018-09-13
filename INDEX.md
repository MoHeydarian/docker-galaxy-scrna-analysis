To generate docker image with UMI tools suite and tools for downstream processing of single cell RNA-seq data.

The `tools.yml` file has the toolshed information required to install the suite of UMI tools when creating the Docker image. This Docker image is a version of Galaxy with the base functionality AND additional tools of single cell analysis. To add additional tools to this Docker image, add them to the `tools.yml` file.

The `Dockerfile` pulls the base Galaxy instance and installs the  additional tools and then creates a Docker image.

The following command generates the Docker image:
$docker build -t scrnagalaxy .


The following command launches the docker image:
$docker run -d -p 8080:80 scrnagalaxy