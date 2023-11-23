**README**

The scripts get_ENA_xml_files.py and get_umbrella_xml.py work with python3, the only additional requirement is the module JINJA2. 

**USAGE**

usage: get_ENA_xml_files.py [-h] -f FILES [-p {ERGA-BGE,CBP,ERGA-pilot,EASI,other}]
                            [-x {all,study,experiment,runs} [{all,study,experiment,runs} ...]] -o OUT_PREFIX

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

**EXAMPLES**

- Phakellia, ERGA-pilot:
`` get_ENA_xml_files.py -f examples/sponge.runs.tsv -p ERGA-pilot -o odPhaVent``

- Valencia hispanica, ERGA_BGE:
``  get_ENA_xml_files.py -f examples/fValHis.runs.tsv -p ERGA-BGE -o fValHis1 ``
