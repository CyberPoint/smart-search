# smart-search
This is a forensic utility written in Python for searching file(s) for keyword
matches. This script is designed to be run from a live Linux instance that you 
are using for analyzing your digital image collections. 

# Setup
To setup your live instance to run this utility you should run the following:


    developer@ubnt20:~/workspace/smart-search$ make develop
    sudo apt-get -y install python3.8 python3-pip pandoc texlive-latex-base texlive-fonts-recommended texlive-fonts-extra texlive-latex-extra upx
    [sudo] password for developer: 
    Reading package lists... Done
    Building dependency tree       
    Reading state information... Done
    ...
    WARNING: The script wheel is installed in '/home/developer/.local/bin' which is not on PATH.
    Consider adding this directory to PATH or, if you prefer to suppress this warning, use --no-warn-script-location.
    Successfully installed setuptools-51.1.1 wheel-0.36.2


# Example
The following example shows how to run this utility:

    developer@ubnt20:~/workspace/smart-search$ scripts/smartsearch -t '~/**/*.docx' -w <WORD LIST>
    03/02/2022 08:39:23 PM reading client properties
    03/02/2022 08:39:23 PM full path to client configuration file is /home/developer/.src/smartsearch.ini
    [
        "/home/developer/Documents/cato_overview_0.10.14.docx"
    ]

    You can supply a list of words or a file that contains a list of words for the -w argument. 
    