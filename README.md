# Docker Taverna Workbench

Docker Taverna Workbench is the junction of two softwares:

***Apache Taverna*** is an open source software tool for designing and executing workflows, initially created by the myGrid project under the name ***Taverna Workbench***, now a project under the Apache incubator. Taverna allows users to integrate many different software components, including WSDL SOAP or REST Web services, such as those provided by the National Center for Biotechnology Information, the European Bioinformatics Institute, the DNA Databank of Japan (DDBJ), SoapLab, BioMOBY and EMBOSS. The set of available services is not finite and users can import new service descriptions into the Taverna Workbench.

***Docker*** is an open-source project that automates the deployment of applications inside software containers, by providing an additional layer of abstraction and automation of operating-system-level virtualization on Linux. Docker uses the resource isolation features of the Linux kernel such as cgroups and kernel namespaces, and a union-capable filesystem such as aufs and others to allow independent "containers" to run within a single Linux instance, avoiding the overhead of starting and maintaining virtual machines.

### Taverna Workbench Core

Taverna Workbench Core is an edition of Taverna that includes support for building and executing scientific workflows using general service types, such as WSDL and REST web services, command line tools and scripts (R, Beanshell), user interactions, including support for general data formats like XML and spreadsheets. Other editions of Taverna Workbench extend the Core edition to also include domain-specific service supports and other customizations.

Pull a Taverna Workbench Core container:

```bash
docker pull bigscience/taverna-workbench:core
```

Start a Taverna Workbench Core container:

```bash
docker run -d -p 5901:5901 -p 6901:6901 \
--name taverna-workbench-core -h taverna-workbench-core \
bigscience/taverna-workbench:core
```

![Taverna](http://i.imgur.com/r9LdKlx.png)

### Taverna Workbench Bioinformatics

Taverna Workbench Bioinformatics is an edition of Taverna Workbench that includes support for building and executing bioinformatics workflows using bioinformatics data and analytical services such as BioMart and BioMoby.

Taverna Workbench Bioinformatics is equivalent to the Taverna Workbench Core bundled with BioMart, BioMoby, SoapLab and API Consumer plugins.

Pull a Taverna Workbench Core container:

```bash
docker pull bigscience/taverna-workbench:bioinformatic
```

Start a Taverna Workbench Core container:

```bash
docker run -d -p 5901:5901 -p 6901:6901 \
--name taverna-workbench-bioinformatic -h taverna-workbench-bioinformatic \
bigscience/taverna-workbench:bioinformatic
```

![Taverna](http://i.imgur.com/XRF1MBE.png)

### Taverna Workbench Astronomy

Taverna Workbench Astronomy is an edition of Taverna that includes support for building and executing astronomy workflows based on Virtual Observatory (VO) services and other REST services.

Deep data inspection and visualisation of results is possible using local connectivity and data sharing with VO software like Aladin and TOPCAT using the SAMP messaging protocol, in addition to support for manipulating and displaying VOTables. Taverna Workbench Astronomy also provides transformation tools based on the STIL tool set and the possibility to execute Aladin scripts and macros. Specific support is also included for use of the VAMDC atomic and molecular data center.

Taverna Workbench Astronomy is equivalent to the Taverna Workbench Core (distributed under LGPL 2.1 license) bundled with the plugins AstroTaverna and VAMDC (distributed under the open source license GPL 3).

Pull a Taverna Workbench Core container:

```bash
docker pull bigscience/taverna-workbench:astronomy
```

Start a Taverna Workbench Core container:

```bash
docker run -d -p 5901:5901 -p 6901:6901 \
--name taverna-workbench-astronomy -h taverna-workbench-astronomy \
bigscience/taverna-workbench:astronomy
```

![Taverna](http://i.imgur.com/r9LdKlx.png)

### Taverna Workbench Biodiversity

Taverna Workbench Biodiversity is an edition of Taverna that includes support for building and executing scientific workflows targetting biodiversity services.

This edition includes support for service types such as REST Web services, WebDAV servers, command line tools, scripts and user interactions, and adds integration with the BiodiversityCatalogue. Taverna Workbench Biodiversity is used by projects like BioVeL, which provide the BioVeL Portal for Web execution of Taverna biodiversity workflows.

Taverna Workbench Biodiversity is equivalent to the Core edition bundled with the plugins for the Service Catalogue and WebDAV.

Pull a Taverna Workbench Core container:

```bash
docker pull bigscience/taverna-workbench:biodiversity
```

Start a Taverna Workbench Core container:

```bash
docker run -d -p 5901:5901 -p 6901:6901 \
--name taverna-workbench-biodiversity -h taverna-workbench-biodiversity \
bigscience/taverna-workbench:biodiversity
```

![Taverna](http://i.imgur.com/r9LdKlx.png)

### Docker container

Docker Taverna Workbench use container BioDesktop Ubuntu. 

[BioDesktop](https://hub.docker.com/r/bigscience/biodesktop/) is a Linux container specifically designed for enabling open science. It is a free and open source operating system based on Ubuntu 15.10 and CentOs 7.2. BioDesktop is the junction of two softwares: Docker container and a Linux operating system.

### Contributing

You are invited to contribute new features, fixes, or updates, large or small; we are always thrilled to receive pull requests, and do our best to process them as fast as we can.

Before you start to code, we recommend discussing your plans through a GitHub issue, especially for more ambitious contributions. This gives other contributors a chance to point you in the right direction, give you feedback on your design, and help you find out if someone else is working on the same thing.

### Author

Current development is led by Fabiano Menegidio.

