# Day 02 - JupyterLab Production Configuration & Triage

## Objective

Configure a hosted JupyterLab server to satisfy specific network ports, proxy routing constraints, and workspace storage directories.

## Tasks Completed

- Checked and ensured the physical existence of the notebook root workspace directory
- Corrected the Jupyter configuration file to bind the server to all network interfaces (`0.0.0.0`)
- Configured the server to listen on the correct port (`8888`)
- Isolated the application root workspace path to `/root/notebooks/`
- Successfully launched the JupyterLab server from the virtual environment

## Commands Used

```bash
mkdir -p /root/notebooks/
source /root/code/ml-env/bin/activate
jupyter lab --config=/root/code/jupyter_lab_config.py --allow-root --no-browser &
```

## What I Learned

- Configuring network host bindings (`0.0.0.0`) to allow access through cloud proxies
- Setting custom infrastructure ports and workspace paths in Jupyter configuration scripts
- The importance of pre-provisioning storage paths before booting an application layer
