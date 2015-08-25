Flash:
	...
	ExternalInterface.addCallback( "setVpConfig" , onVpConfigCalled );
	function onVpConfigCalled( data:object ):void{
		// do something with de Vp data
	}
	...
	broadcastEventExternally( 'getVpData' );
	...

JS:
	var vpConfig = {...};
	...
	player.on( 'getVpData' , function(){
		player.el().setVpConfig( vpConfig );
		// Alternate method
		// player.el().vjs_setProperty('vpConfig')
	});
	...
