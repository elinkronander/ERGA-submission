**USAGE**

./get_ENA_xml_files.py -h


usage: get_ENA_xml_files.py [-h] -f FILES


                            [-p {ERGA-BGE,CBP,ERGA-pilot,EASI,other}]


                            [-x {all,study,experiment,runs} [{all,study,experiment,runs} ...]]


                            -o OUT_PREFIX





options:


  -h, --help            show this help message and exit


  -f FILES, --files FILES


                        TABLE file with appropriate headers


  -p {ERGA-BGE,CBP,ERGA-pilot,EASI,other}, --project {ERGA-BGE,CBP,ERGA-pilot,EASI,other}


                        project


  -x {all,study,experiment,runs} [{all,study,experiment,runs} ...], --xml {all,study,experiment,runs} [{all,study,experiment,runs} ...]


                        specify which xml files do you want


  -o OUT_PREFIX, --out_prefix OUT_PREFIX


                        prefix to add to output files
