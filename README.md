# NxtDevKit for Javascript
Javascript development framework for Nxt. Create transactions with Javascript, get the most used Nxt functions. 

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
