RUDICS CALL ORDER OF OPERATIONS

    Wave Glider receives a wake-up command to initiate a rudics call (30 seconds)

        This can be initiated by a sensor producing a file and sending it to PPPHost (VM4 for example attempts to do this)

        More commonly this is initiated by the set time interval provided by the PPPHost-config.xml file.

    Wave Glider begins connection to the rudics server. [./runppp  (1 to 4min)]

    Wave Glider connects to rudics and initiates an SCP function to PSNxxxxx@smc.wgms.com. [./runscp (1min)]

    Wave Glider connects via SCP to remote server.

    Remote server initiates ./runme script server side to initiate user defined functions (time dependent on file offload)

    ./runme executes VRL data download, organizes based on last modified date, and copys the files to our remote server; parses, organizes based on date, sets a bookmark for data truncation, and sends parsed real time tag events as a .csv.
