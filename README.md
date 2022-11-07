# galaxy-tool-split-on-primer

Demultiplex sequences bases on (mid)label; substitution (hamming) and fuzzy (levenshtein) string searches  
are used to pinpoint label position. Each (mid)label (if present) will yield an output file. This repo uses Python3  
and has been tested with Galaxy v.22.01 (using a Terraform/Ansible install on the new Naturalis OpenStack).

## Installation
### Manual
Clone this repo in your Galaxy ***Tools*** directory:  
`git clone https://github.com/naturalis/galaxy-tool-split-on-primer`  

Make the python script executable:  
`chmod 755 galaxy-tool-split-on-primer/Split_on_Primer.sh`  
`chmod 755 galaxy-tool-split-on-primer/Split_on_Primer.py` 

Append the file ***tool_conf.xml***:    
`<tool file="/path/to/Tools/galaxy-tool-split-on-primer/Split_on_Primer.sh" />`  

### Ansible
Depending on your setup the [ansible.builtin.git](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/git_module.html) module could be used.  
[Install the tool](https://docs.ansible.com/ansible/latest/collections/ansible/builtin/git_module.html#examples) by including the following in your dedicated ***.yml** file:  

`  - repo: https://github.com/naturalis/galaxy-tool-split-on-primer`  
&ensp;&ensp;`file: Split_on_Primer.xml`  
&ensp;&ensp;`version: master`  

## Usage
Information on tool usage, parameters and examples can be found [here](https://github.com/naturalis/galaxy-tool-split-on-primer/blob/master/usage.md)  

## Source
https://github.com/Y-Lammers/Split_on_Primer
