# NxtDevKit for Javascript
Javascript development framework for Nxt. Create transactions with Javascript, get the most used Nxt functions. 

# Why?

The NxtDevKit is a light version of the full NRS which was developed by Nxt developers to work with the Nxt API and JavaScript.
The NRS finds the local Nxt instance, any transaction that will go through the wrapper will be signed locally and then submitted to Nxt.

No passphrase will leave your JavaSscript, check NRS.sendRequest

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
			$.growl($.t("error_search_no_results"), {
				"type": "danger"
			});
		}
	});
