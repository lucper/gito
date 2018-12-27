
![Gito](https://raw.githubusercontent.com/gitobioinformatics/gito/master/gito.png)

# GITO - A lightweight and safe container for bioinformatics

### Full Description:

GITO, a lightweight and safe container docker image based on [Alpine](https://alpinelinux.org) containing bioinformatics tools ready to be used. The base image is only 4.41 MB in size and contains only the OS libraries and language de-pendencies required to run an application, but robust enough to run bioinformatics pipeline with security.

GITO is an open source using the [Docker platform](https://www.docker.com) and provides an easy and modular method for building, distributing, and replicating pipelines, which has a base image (GITO-base) that forms the single foundation layer on which each container application is built.
GITO adopts "start with minimum and add dependencies as needed" approach, which have separate containers for each bioinformatics tool with the minimum to run. GITO use musl as the standard C library for Linux-based systems, 
called [musl-libc](https://www.musl-libc.org). Musl-libc is free, lightweight, security-oriented and smaller in size compared to 
the Glibc library. The source code for bioinformatics tools, written in C, C ++ and Java, has been compiled for native Alpine executables.



---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Guide to downloading and running this Docker image
#### Step 1: Install Docker

To download and run this Docker image, you first need to set up Docker on your machine. The easiest way to start with Docker is to install the [Docker Toolbox](https://www.docker.com/products/docker-desktop) by simply 
 downloading and clicking the installer which is available for both Mac OSX and Windows. For Linux users, follow the 
 instructions [here](https://docs.docker.com/get-started/).
 
#### Step 2: Download and run the Docker image

Option 1: Through a Command Line Interface (CLI)
            The image can be downloaded and executed through the CLI of Docker's Docker Quickstart Terminal in the [Docker Toolbox](https://www.docker.com/products/docker-desktop) with the following commands:

   1.  Pull(download) the Docker images:
   
        $ docker pull gitobioinformatics/fastqc
        
        $ docker pull gitobioinformatics/trimmomatic
        
        $ docker pull gitobioinformatics/trinity
        
        $ docker pull gitobioinformatics/bowtie2


   2.  Change the working directory to a project, and run the following commands:
   
       > Run FastQC
       
       $ docker run -v $PWD:$PWD --rm gitobioinformatics/fastqc

       > Run Trimmomatic
       
       $ docker run -v $PWD:$PWD --rm gitobioinformatics/trimmomatic

       > Run Trinity
       
       $ docker run -v $PWD:$PWD --rm gitobioinformatics/trinity

       > Run Bowtie2
       
       docker run -v $PWD:$PWD --rm gitobioinformatics/bowtie2

#### Deploy this Docker image onto your cloud
You can download and deploy this Docker image with your cloud provider such as DigitalOcean, Amazon Web Services, HP Enterprise, IBM, Microsoft Azure Cloud or others.



---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### Reproducing a pipeline example
GITO was used to reproduce the pipeline present in the work of Hernández-Fernández (2017), which is the first de novo transcriptome assembly of [Eretmochelys imbricate published](https://doi.org/10.1016/j.dib.2017.10.015), instructions used and execution results can be [accessed here](https://github.com/gitobioinformatics/gito/tree/master/examples/eretmochelys_imbricata).

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### GITO's security analysis

We used [Quay Security Scanner](https://quay.io) to assess vulnerabilities in the GITO. Quay identifies insecure packages by matching the metadata against Common Vulnerabilities and Exposures (CVE) vulnerability database. After the analysis, the Quay software did not identify any vulnerability in GITO, neither in the base image nor in the images with the tools used in the pipeline.The results of the analysis can be found here

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### License

MIT License. See [License.txt](https://raw.githubusercontent.com/gitobioinformatics/gito/master/MIT%20License.txt) for more information

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Contributions
GITO is open-source (see License), and we welcome contributions from anyone who is interested in contributing. To contribute code, please make a pull request on github. The issue tracker for GITO is also available on github.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Inspirations
The word "gito" is used by populations of the North of Brazil when people refer to something "very small, smaller than normal".
The logo of the project was inspired by the Boto Tucuxi (Sotalia fluviatilis), which is one of the smallest dolphins in the Delphinidae family and the only one of this family that lives in rivers. It is a very agile dolphin, although it is an endangered species, it is still possible to find it in the rivers of the Amazon jumping in the air.

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Acknowledgements
We thank the following institutions, which contributed to ensuring the success of our work:<br>

Ministério da Ciência, Tecnologia, Inovação e Comunicação (MCTIC)
    
Museu Paraense Emílio Goeldi (MPEG)
    
Centro Universitário do Estado do Pará (CESUPA)

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Funding
This work has been supported by Conselho Nacional de Desenvolvimento Científico e Tecnológico - CNPq (grants 149985/2018-5; 129954/2018-7)

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
### Authors
 Marcos Paulo Alves de Sousa<br>
 Franklin Gonçalves Sobrinho <br>
 Lucas Peres Oliveira <br>
 Kayke Correa Conceição Lins Pereira
 
 ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 ### Contact
 Dr. Marcos Paulo Alves de Sousa (Project leader)<br>
 
 <i><b>Email:</b> msousa@museu-goeldi.br<br>
 Laboratório de Biologia Molecular<br>
 Museu Paraense Emílio Goeldi<br>
 Av. Perimetral 1901. CEP 66077- 530. Belém, Pará, Brazil.</i>
