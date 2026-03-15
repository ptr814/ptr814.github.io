# TMF8829 JSON Logfile HTML converter

This repository copies content from https://github.com/ams-OSRAM/tmf8829_json_logfile_viewer and modifies
execution to run the scripts inside JupyterLite. Example to convert all json.gz files to html files:

```python
%run json_to_html.py -i .
```

This tool enables the easy conversion of JSON logfile outputs to html for interactive viewing of

* Distance information in physical distance and x/y/z
* Noise, crosstalk (xtalk), SNR and signal amplitude of each pixel
* Histogram data for the pixels (MP) and reference (Ref)

inside a browser.

A typical output is shown below:
![video](https://raw.githubusercontent.com/ams-OSRAM/tmf8829_json_logfile_viewer/refs/heads/main/media/operation.gif)

## Additional tools

### split_json

Split JSON files into smaller files.

### json_to_csv

JSON to csv converter - e.g. for using with excel.

## Howto use

JSON logfiles can be created using the ams-OSRAM evaluation software downloaded from https://ams-osram.com/tmf8829 - see the user guide for the EVM howto create these files.

Alternatively JSON logfiles can be created with [tmf8829_zeromq_client.py](https://github.com/ams-OSRAM/tmf8829_driver_python/blob/main/tmf8829/zeromq/tmf8829_zeromq_client.py) or the exe program inside TMF8829_Driver_ZMQ_Server_Client_EXE_v-latest-version.zip from https://ams-osram.com/tmf8829 website.

### Inside JupyterLite .ipynb file
Create a JupyterLite file and replace 'tmf8829_log_1770799073' with your actual logfile.

```python
# JSON to HTML conversion
%run json_to_html.py -i tmf8829_log_1770799073.json.gz

# split JSON file into smaller files with 10 measurements
%run split_json.py -i tmf8829_log_1770799073.json.gz -n 10

# JSON to CSV conversion
%run json_to_csv.py tmf8829_log_1770799073.json.gz tmf8829_log_1770799073.csv
```

and open the created html file *tmf8829_log_1770799073._viewer.html* inside JupyterLite
and allow 'Trust HTML':

![image](https://raw.githubusercontent.com/ams-OSRAM/tmf8829_json_logfile_viewer/refs/heads/main/media/operation_jupyterlab.png)

