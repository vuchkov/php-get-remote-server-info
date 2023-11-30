# php-get-remote-server-info

## Get the remote hosting server info in PHP language.

```
ob_start(); // Turn on output buffering
system('ifconfig'); // or other console command information as an example: fisk free space.
$mycom=ob_get_contents();
ob_clean();
$findme = "Physical";

$pmac = strpos($mycom, $findme);
$mac=substr($mycom,($pmac+36),17); 
echo $mac;
```
