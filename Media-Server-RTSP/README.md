Overview
--------
<p>This plugin converts an XD or 4K player to a Media Server that waits for clients to connect, and then starts streaming to them. When the files being streamed are cached (i.e. they aren't being read from the SD card), XD players support up to four 19Mbps streams. 4K players support up to 50 19Mbps streams of the same file or 11 streams (16Mbps average) of different files.</p>
<p>The Media Server currently only supports MPEG-2 transport stream files.</p>

Details
-------------
<p>rtsp server, port 8090 (the port number can be changed if needed)</p>
<p>Streaming File from Client: rtsp://ServerIpAddress:8090/file:///folder/file.ts</p>
<p>rtsp://ServerIpAddress:8090/file:///file.ts</p>

Server Parameters
------------------
<p><strong>Maxbitrate</strong></p>
<p>Sets the maximum instantaneous bitrate of the RTP transfer initiated by RTSP. This has no effect for HTTP. The units are in Kbps; the parameter value 80000 (meaning 80Mbps) has been found to work well for streaming to XD players. The default behaviour (achieved by passing the value zero) is to not limit the bitrate at all.</p>

<p>Example: "rtsp:port=554&trace&maxbitrate=80000"</p>

<p><strong>Threads</strong></p>
<p>Each thread handles one client; the default value is "5".</p>

<p>Example: "http:port=8080&threads=10"</p>
