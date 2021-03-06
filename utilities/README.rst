=====
Usage
=====

To use link_fastq_juno.py from cli::

Usage: link_fastq_juno.py [OPTIONS]

Options:
  -m, --manifest-file PATH        Manifest file having information about run
                                  id and sample id to get the fastq files (eg:
                                  -m Project_05500_GB_manifest.xslx)
                                  [required]
  -p, --request-id TEXT           IGO request id to get the fastq files.
                                  (eg:-p Project_05500_GB or -p 05500_GB)
                                  [required]
  -fp, --fastq-path PATH          Full path to fastq files  [required]
  -op, --output-path PATH         Full path to where we link the output files
                                  [required]
  -cp, --cutadapt-path PATH       Full path to location of cutadapt executable
                                  [required]
  -pfp, --process-fastq-path PATH
                                  Full path to location of cutadapt executable
                                  [required]
  -l, --expected-read-length INTEGER
                                  Expected read length from the fastq file
  --version                       Show the version and exit.
  -v, --verbosity LVL             Either CRITICAL, ERROR, WARNING, INFO or
                                  DEBUG
  --help                          Show this message and exit.

Example commandline:

    .. code-block:: console
    
       $ python3 link_fastq_juno.py \
       -p request_id \
       -m /path/to/manifest.xlsx \
       -pfp /path/to/process_fastq \
       -fp /path/to/fastq/directory \
       -op /path/to/output/directory \
       -cp /path/to/cutadapt
    
    .. code