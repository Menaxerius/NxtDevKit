# NxtDevKit for Javascript
Javascript development framework for Nxt. Create transactions with Javascript, get the most used Nxt functions. 

# Why?

The NxtDevKit is a light version of the full NRS which was developed by Nxt developers to work with the Nxt API and JavaScript.
The NRS finds the local Nxt instance, any transaction that will go through the wrapper will be signed locally and then submitted to Nxt.

No passphrase will leave your JavaSscript, check NRS.sendRequest

# Documentation & Installation

Extraced from NRS Version 1.7.5 https://nxtforum.org/nrs-releases/nrs-v1-7-5/
Please install Nxt locally and open cors in the configuration as explained here:

	# Enable Cross Origin Filter for the API server.
	nxt.apiServerCORS=true
	​
	# Enable Cross Origin Filter for NRS user interface server.
	nxt.uiServerCORS=true

https://medium.com/@Damelon/coding-for-nxt-crypto-platform-1-c3580b4cfd38#.vwf0q0b2a


# Nxt Api

When Nxt is running go to: http://localhost:7876/test

Wiki documentation:

http://nxtwiki.org/wiki/The_Nxt_API

# Use NRS functions

use NRS functions, to submit Nxt requests:

# Examples

	 NRS.sendRequest("getBlockchainStatus", {
					
	}, function(response, input) {
		if (!response.errorCode) {
			console.log(response);
			console.log(input);

			$("#blockchainStatus").html('Current Block: '+response.numberOfBlocks+' - Current Nxt Time '+response.time);

		} else {
			console.log('Could not connect to Nxt. Please enable cors like explained on https://github.com/Tosch110/NxtDevKit');
		}
	});
