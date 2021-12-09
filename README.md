# node-red-contrib-custom-websocket
custom websocket node implementation for node-red

## To-do
- Check query parameters in websocket server handleUpgrade(below code is as-is, query parameters can be handled!)
~~~
var url = require('url');
url.parse('http://localhost:8080/test?param1=val1&param2=val2')
Url {
  protocol: 'http:',
  slashes: true,
  auth: null,
  host: 'localhost:8080',
  port: '8080',
  hostname: 'localhost',
  hash: null,
  search: '?param1=val1&param2=val2',
  query: 'param1=val1&param2=val2',
  pathname: '/test',
  path: '/test?param1=val1&param2=val2',
  href: 'http://localhost:8080/test?param1=val1&param2=val2'
}
~~~

- Add custom header to set when connecting websocket client(use header to specific purpose like Authentication, below code is as-is)
~~~
var options = {};
if (agent) {
    options.agent = agent;
}
if (node.tls) {
    var tlsNode = RED.nodes.getNode(node.tls);
    if (tlsNode) {
        tlsNode.addTLSOptions(options);
    }
}
var socket = new ws(node.path,options);
~~~
