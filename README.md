< div  id = " streamroot-graphs " > </ div >
< script  src = " https://tools.streamroot.io/usage-graphs/latest/graphs.js " > </ script >
< html >
< tête >

  <! - video.js -> 
  < link  href = " //vjs.zencdn.net/5.8/video-js.min.css "  rel = " stylesheet " >
  < script  src = " //vjs.zencdn.net/5.8/video.min.js " > </ script >

  <! - script videojs-contrib-dash -> 
  < script  src = " dist / videojs5-dashjs-p2p-source-handler.js " > </ script >
</ head >
< body >
  < div >
      < video  id = " video_element "  width = " 480 "  height = " 360 "  contrôle la  sourdine  class = " video-js vjs-default-skin " />
  </ div >

  < script >

    var options = { 
        html5 : { 
            dash : { 
              limitBitrateByPortal :  true , 
              debugLogToConsole :  true
             }, 
            streamroot : { 
                p2pConfig : { 
                    streamrootKey :  " YOUR_STREAMROOTKEY_HERE "
                 } 
            } 
        } 
    };

    var player =  videojs ( ' video_element ' , options); 
      

  < div  id = " streamroot-graphs " > </ div >
  < script  src = " https://tools.streamroot.io/usage-graphs/latest/graphs.js " > </ script >
</ body >
</ html >
si ( ! Options ||  ! les options . streamroot  ||  ! les options . streamroot . p2pConfig ) {
   lancer une  nouvelle  erreur ( ' p2pConfig n'est pas défini! ' );
}

// initialisation de streamroot-p2p-bundle 
this . mediaPlayer_  =  DashjsP2PBundle . MediaPlayer ( Html5DashJS . Context_ ). créer ( options . streamroot . p2pConfig );
dnaConfig: {  "backendUrl": "distributor.mywebsite.com"}
